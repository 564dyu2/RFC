# Specification

|         |                                                                         |
|:------- | ----------------------------------------------------------------------- |
| Title   | Remote access for Chronicle Engine                                      |
| Parent  | https://github.com/OpenHFT/RFC/blob/master/Chronicle/Engine             |
| URL     | https://github.com/OpenHFT/RFC/blob/master/Chronicle/Engine/Remote      |
| Latest  | https://github.com/OpenHFT/RFC/blob/master/Chronicle/Engine/Remote/Remote-Chronicle-Engine-0.1.md |
| Editor  | Peter Lawrey                                                            |
| License | Apache 2.0                                                              |
| Change Process | Users issue Pull Requests for the Editor's consideration.        |
| Status  | Raw.                                                                    |

# Goals
An RFC for library specific requirements for Remote access to a Chronicle Engine. See the parent RFC for cross library requirements.

## Session level messages
Session messages are [Size Prefixed Blob](https://github.com/OpenHFT/RFC/blob/master/Size-Prefixed-Blob/) which don't need meta-data as they are sent directly to the session.

If meta data has been sent, this can be reset by sending an empty meta data message.  This message can be used as a heartbeat.

```yaml
# clear the meta data routing
--- !!meta-data
# nothing.
...
```

## Header
When a TCP connection is established a `header` and `header-reply` is sent as hand shaking.

```yaml
# no meta-data selected as this is session level data.
--- !!data
header: {
    engine-version: 3.0.0-alpha-SNAPSHOT
    wire-formats: [ Raw, Binary, Text ]
}
...
```

If the engine versions match, the first matching `wire-formats` can be used.
If the versions don't match, `Raw` cannot be used as it is not schema change tolerant.

```yaml
--- !!data
header-reply: {
    wire-format: Binary
}
```

### Connection footer
A connection can disconnect gracefully and give a message for logging purposes.
```yaml
--- !!meta-data
# no meta data indicate that this is a session message
....
--- !!data
bye: { message: Timed out }
...
```

## Service lookup
To get the URI for a relative URI name, you can contact the service-lookup service.

```yaml
--- !!meta-data
csp:///service-lookup
tid: 1426502826520
...
--- !!data
lookup: { relativeUri: myMap, view: !Map }
...
```

The reply may lookup like
```yaml
--- !!meta-data
tid: 1426502826520
...
--- !!data
lookup-reply: { relativeUri: myMap, view: !Map, uri: "csp://server1/myMap" }
...
```

The underlying API in Java could lookup like
```java
public interface ServiceLookup {
    public Future<LookupReply> lookup(Lookup lookupRequest);
}

public interface Lookup {
    public String getRelativeUri();
    public void setRelativeUri(String relativeUri);
    public String getView();
    public void setView(String view);
}

public interface LookupReply {
    public String getRelativeUri();
    public void setRelativeUri(String relativeUri);
    public String getView();
    public void setView(String view);
    public URI getUri();
    public void setUri(URI uri);
}
```

To use this service, the meta data block would look like
```yaml
--- !!meta-data
csp://server1/myMap
tid: 1426502826525
...
--- !!data
keySet:
...
```

to which the reply could be
```yaml
--- !!meta-data
tid: 1426502826525
...
--- !!data !Proxy
csp://server1/myMap#keySet
type: !Set
...
```

The `!proxy` specifies the reply is a `Proxy` of type `Set` which points to the `keySet` of the map.

# The Context API
Each of these messages call the service lookup and expect to return the actual service if performed locally,
or a proxy if performed remotely.  Whether the code is run remotely or locally, it should appear to behave the same way.

```java
public interface ChronicleContext {

    <K, V> ChronicleMap<K, V> getMap(String name, Class<K> kClass, Class<V> vClass);

    <E> ChronicleSet<E> getSet(String name, Class<E> eClass);

    <I> I getService(Class<I> iClass, String name, Class... args);
}
```

## Example
This code results in two requests.  One to get the service, if it is not already cached, and one to perform the action.
```java
ChronicleMap<Integer, String> map = context.getMap("test", Integer.class, String.class);

map.put(1, "hello");
map.put(2, "world");
map.put(3, "bye");
```

The service lookup, client to server
```yaml
--- !!meta-data
csp:///service-lookup
tid: 1426502826520
...
--- !!data
lookup: { relativeUri: test, view: !Map, types: [ !Integer, !String ] }
...
```
... and the reply server to client.

```yaml
--- !!meta-data
tid: 1426502826520
...
--- !!data
lookup-reply: { relativeUri: myMap, view: !Map, types: [ !Integer, !String ], uri: "csp://server1/test", cid: 1 }
...
```
In this case, the `cid` is the channelId.  This can be used as a short hand of the `uri`

```yaml
--- !!meta-data
cid: 1
# or
csp://server1/test
tid: 1426502826525
...
--- !!data
put: { key: 1, value: hello }
...
--- !!data
put: { key: 2, value: world }
...
--- !!data
put: { key: 3, value: bye }
...
```

This `put` assumes a reply for each put in order.  An `async-put` may be required for avoid a reply.