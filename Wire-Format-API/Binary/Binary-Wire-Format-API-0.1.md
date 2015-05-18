# Goals

A compact encoding that both desicrbes the the length of the fields and the type of the fields.

See example below

# Examples

these examples are based on bits

| comment                               | 7   | 6   | 5   | 4   | 3   | 2   | 1   | 0  |
| ------------------------------------- | --- | --- | --- | --- | --- | --- | --- | ---|
| top three bits denotes a three Type   | x   | x   | x   |  x  |     |     |     |    |
| remaining bits dente the size         |     |     |     |     | x   | x  |  x   | x  |


## Types

| comment                               | 7   | 6   | 5   | 4   | 3   | 2   | 1   | 0  |
| ------------------------------------- | --- | --- | --- | --- | --- | --- | --- | ---|
| Num (0-15)                            | 0   | 0   | 0   | 0   |     |     |     |    | 
| Num (16-31)                           | 0   | 0   | 0   | 1   |     |     |     |    | 
| Num (32-47)                           | 0   | 0   | 1   | 0   |     |     |     |    | 
| Num (48-63)                           | 0   | 0   | 1   | 1   |     |     |     |    | 
| Num (64-79)                           | 0   | 1   | 0   | 0   |     |     |     |    | 
| Num (80-95)                           | 0   | 1   | 0   | 1   |     |     |     |    | 
| Num (96-111)                          | 0   | 1   | 1   | 0   |     |     |     |    | 
| Num (112-127)                         | 0   | 1   | 1   | 1   |     |     |     |    | 
| Control Message                       | 1   | 0   | 0   |     |     |     |     |    | 
| Decimal                               | 1   | 1   | 1   |     |     |     |     |    | 
| Integer                               | 1   | 1   | 0   |     |     |     |     |    | 
| Special                               | 1   | 1   | 0   |     |     |     |     |    | 
| String                                | 1   | 1   | 1   |     |     |     |     |    |
| Field                                 | 1   | 0   | 0   |     |     |     |     |    | 
