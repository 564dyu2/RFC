#Binary Wire Examples

### Get
example of get(<key>) returning null, when the keys is not present in the map

sends:

```yaml
00000000 23 00 00 40 B9 03 63 73  70 EF 2F 2F 74 65 73 74 #··@··cs p·//test
00000010 3F 76 69 65 77 3D 4D 41  50 B9 03 74 69 64 A7 18 ?view=MA P··tid··
00000020 E0 46 AF 4D 01 00 00 06  00 00 00 B9 03 67 65 74 ·F·M···· ·····get
00000030 2A                                               *                
```

receives:

```yaml
00000000 08 00 00 00 B9 05 72 65  70 6C 79 BB             ······re ply·    
```

### Contains Key _ Null Pointer Exception
c.containsKey(null) will throw a NullPointerException

sends:

```yaml
00000000 23 00 00 40 B9 03 63 73  70 EF 2F 2F 74 65 73 74 #··@··cs p·//test
00000010 3F 76 69 65 77 3D 4D 41  50 B9 03 74 69 64 A7 A7 ?view=MA P··tid··
00000020 F0 46 AF 4D 01 00 00 0E  00 00 00 B9 0B 63 6F 6E ·F·M···· ·····con
00000030 74 61 69 6E 73 4B 65 79  BB                      tainsKey ·       
```

receives:

```yaml
00000000 BA 0A 00 00 B9 09 65 78  63 65 70 74 69 6F 6E B6 ······ex ception·
00000010 1E 6A 61 76 61 2E 6C 61  6E 67 2E 4E 75 6C 6C 50 ·java.la ng.NullP
00000020 6F 69 6E 74 65 72 45 78  63 65 70 74 69 6F 6E 82 ointerEx ception·
00000030 8A 0A 00 00 C7 6D 65 73  73 61 67 65 BB CA 73 74 ·····mes sage··st
00000040 61 63 6B 54 72 61 63 65  82 71 0A 00 00 82 69 00 ackTrace ·q····i·
00000050 00 00 C5 63 6C 61 73 73  B8 2F 6E 65 74 2E 6F 70 ···class ·/net.op
00000060 65 6E 68 66 74 2E 63 68  72 6F 6E 69 63 6C 65 2E enhft.ch ronicle.
00000070 65 6E 67 69 6E 65 2E 6D  61 70 2E 4D 61 70 57 69 engine.m ap.MapWi
00000080 72 65 48 61 6E 64 6C 65  72 C6 6D 65 74 68 6F 64 reHandle r·method
00000090 E9 6E 75 6C 6C 43 68 65  63 6B C4 66 69 6C 65 F3 ·nullChe ck·file·
000000a0 4D 61 70 57 69 72 65 48  61 6E 64 6C 65 72 2E 6A MapWireH andler.j
000000b0 61 76 61 C4 6C 69 6E 65  A2 85 01 82 71 00 00 00 ava·line ····q···
000000c0 C5 63 6C 61 73 73 B8 31  6E 65 74 2E 6F 70 65 6E ·class·1 net.open
000000d0 68 66 74 2E 63 68 72 6F  6E 69 63 6C 65 2E 65 6E hft.chro nicle.en
000000e0 67 69 6E 65 2E 6D 61 70  2E 4D 61 70 57 69 72 65 gine.map .MapWire
000000f0 48 61 6E 64 6C 65 72 24  31 C6 6D 65 74 68 6F 64 Handler$ 1·method
00000100 F0 6C 61 6D 62 64 61 24  61 63 63 65 70 74 24 32 ·lambda$ accept$2
00000110 32 C4 66 69 6C 65 F3 4D  61 70 57 69 72 65 48 61 2·file·M apWireHa
00000120 6E 64 6C 65 72 2E 6A 61  76 61 C4 6C 69 6E 65 A1 ndler.ja va·line·
00000130 FC 82 69 00 00 00 C5 63  6C 61 73 73 B8 46 6E 65 ··i····c lass·Fne
00000140 74 2E 6F 70 65 6E 68 66  74 2E 63 68 72 6F 6E 69 t.openhf t.chroni
00000150 63 6C 65 2E 65 6E 67 69  6E 65 2E 6D 61 70 2E 4D cle.engi ne.map.M
00000160 61 70 57 69 72 65 48 61  6E 64 6C 65 72 24 31 24 apWireHa ndler$1$
00000170 24 4C 61 6D 62 64 61 24  36 35 2F 37 38 31 34 34 $Lambda$ 65/78144
00000180 35 37 37 30 C6 6D 65 74  68 6F 64 E6 61 63 63 65 5770·met hod·acce
00000190 70 74 C4 66 69 6C 65 BB  C4 6C 69 6E 65 A4 FF 82 pt·file· ·line···
000001a0 73 00 00 00 C5 63 6C 61  73 73 B8 2F 6E 65 74 2E s····cla ss·/net.
000001b0 6F 70 65 6E 68 66 74 2E  63 68 72 6F 6E 69 63 6C openhft. chronicl
000001c0 65 2E 65 6E 67 69 6E 65  2E 6D 61 70 2E 4D 61 70 e.engine .map.Map
000001d0 57 69 72 65 48 61 6E 64  6C 65 72 C6 6D 65 74 68 WireHand ler·meth
000001e0 6F 64 F3 6C 61 6D 62 64  61 24 77 72 69 74 65 44 od·lambd a$writeD
000001f0 61 74 61 24 32 35 C4 66  69 6C 65 F3 4D 61 70 57 ata$25·f ile·MapW
00000200 69 72 65 48 61 6E 64 6C  65 72 2E 6A 61 76 61 C4 ireHandl er.java·
00000210 6C 69 6E 65 A2 9D 01 82  67 00 00 00 C5 63 6C 61 line···· g····cla
00000220 73 73 B8 44 6E 65 74 2E  6F 70 65 6E 68 66 74 2E ss·Dnet. openhft.
00000230 63 68 72 6F 6E 69 63 6C  65 2E 65 6E 67 69 6E 65 chronicl e.engine
00000240 2E 6D 61 70 2E 4D 61 70  57 69 72 65 48 61 6E 64 .map.Map WireHand
00000250 6C 65 72 24 24 4C 61 6D  62 64 61 24 36 36 2F 35 ler$$Lam bda$66/5
00000260 31 34 34 31 32 35 32 33  C6 6D 65 74 68 6F 64 E6 14412523 ·method·
00000270 61 63 63 65 70 74 C4 66  69 6C 65 BB C4 6C 69 6E accept·f ile··lin
00000280 65 A4 FF 82 4F 00 00 00  C5 63 6C 61 73 73 B8 20 e···O··· ·class· 
00000290 6E 65 74 2E 6F 70 65 6E  68 66 74 2E 63 68 72 6F net.open hft.chro
000002a0 6E 69 63 6C 65 2E 77 69  72 65 2E 57 69 72 65 73 nicle.wi re.Wires
000002b0 C6 6D 65 74 68 6F 64 E9  77 72 69 74 65 44 61 74 ·method· writeDat
000002c0 61 C4 66 69 6C 65 EA 57  69 72 65 73 2E 6A 61 76 a·file·W ires.jav
000002d0 61 C4 6C 69 6E 65 4E 82  57 00 00 00 C5 63 6C 61 a·lineN· W····cla
000002e0 73 73 B8 22 6E 65 74 2E  6F 70 65 6E 68 66 74 2E ss·"net. openhft.
000002f0 63 68 72 6F 6E 69 63 6C  65 2E 77 69 72 65 2E 57 chronicl e.wire.W
00000300 69 72 65 4F 75 74 C6 6D  65 74 68 6F 64 ED 77 72 ireOut·m ethod·wr
00000310 69 74 65 44 6F 63 75 6D  65 6E 74 C4 66 69 6C 65 iteDocum ent·file
00000320 EC 57 69 72 65 4F 75 74  2E 6A 61 76 61 C4 6C 69 ·WireOut .java·li
00000330 6E 65 44 82 69 00 00 00  C5 63 6C 61 73 73 B8 2F neD·i··· ·class·/
00000340 6E 65 74 2E 6F 70 65 6E  68 66 74 2E 63 68 72 6F net.open hft.chro
00000350 6E 69 63 6C 65 2E 65 6E  67 69 6E 65 2E 6D 61 70 nicle.en gine.map
00000360 2E 4D 61 70 57 69 72 65  48 61 6E 64 6C 65 72 C6 .MapWire Handler·
00000370 6D 65 74 68 6F 64 E9 77  72 69 74 65 44 61 74 61 method·w riteData
00000380 C4 66 69 6C 65 F3 4D 61  70 57 69 72 65 48 61 6E ·file·Ma pWireHan
00000390 64 6C 65 72 2E 6A 61 76  61 C4 6C 69 6E 65 A2 99 dler.jav a·line··
000003a0 01 82 67 00 00 00 C5 63  6C 61 73 73 B8 31 6E 65 ··g····c lass·1ne
000003b0 74 2E 6F 70 65 6E 68 66  74 2E 63 68 72 6F 6E 69 t.openhf t.chroni
000003c0 63 6C 65 2E 65 6E 67 69  6E 65 2E 6D 61 70 2E 4D cle.engi ne.map.M
000003d0 61 70 57 69 72 65 48 61  6E 64 6C 65 72 24 31 C6 apWireHa ndler$1·
000003e0 6D 65 74 68 6F 64 E6 61  63 63 65 70 74 C4 66 69 method·a ccept·fi
000003f0 6C 65 F3 4D 61 70 57 69  72 65 48 61 6E 64 6C 65 le·MapWi reHandle
00000400 72 2E 6A 61 76 61 C4 6C  69 6E 65 A1 C9 82 67 00 r.java·l ine···g·
00000410 00 00 C5 63 6C 61 73 73  B8 31 6E 65 74 2E 6F 70 ···class ·1net.op
00000420 65 6E 68 66 74 2E 63 68  72 6F 6E 69 63 6C 65 2E enhft.ch ronicle.
00000430 65 6E 67 69 6E 65 2E 6D  61 70 2E 4D 61 70 57 69 engine.m ap.MapWi
00000440 72 65 48 61 6E 64 6C 65  72 24 31 C6 6D 65 74 68 reHandle r$1·meth
00000450 6F 64 E6 61 63 63 65 70  74 C4 66 69 6C 65 F3 4D od·accep t·file·M
00000460 61 70 57 69 72 65 48 61  6E 64 6C 65 72 2E 6A 61 apWireHa ndler.ja
00000470 76 61 C4 6C 69 6E 65 A1  AD 82 65 00 00 00 C5 63 va·line· ··e····c
00000480 6C 61 73 73 B8 2F 6E 65  74 2E 6F 70 65 6E 68 66 lass·/ne t.openhf
00000490 74 2E 63 68 72 6F 6E 69  63 6C 65 2E 65 6E 67 69 t.chroni cle.engi
000004a0 6E 65 2E 6D 61 70 2E 4D  61 70 57 69 72 65 48 61 ne.map.M apWireHa
000004b0 6E 64 6C 65 72 C6 6D 65  74 68 6F 64 E7 70 72 6F ndler·me thod·pro
000004c0 63 65 73 73 C4 66 69 6C  65 F3 4D 61 70 57 69 72 cess·fil e·MapWir
000004d0 65 48 61 6E 64 6C 65 72  2E 6A 61 76 61 C4 6C 69 eHandler .java·li
000004e0 6E 65 4E 82 82 00 00 00  C5 63 6C 61 73 73 B8 3E neN····· ·class·>
000004f0 6E 65 74 2E 6F 70 65 6E  68 66 74 2E 63 68 72 6F net.open hft.chro
00000500 6E 69 63 6C 65 2E 65 6E  67 69 6E 65 2E 73 65 72 nicle.en gine.ser
00000510 76 65 72 2E 69 6E 74 65  72 6E 61 6C 2E 45 6E 67 ver.inte rnal.Eng
00000520 69 6E 65 57 69 72 65 48  61 6E 64 6C 65 72 C6 6D ineWireH andler·m
00000530 65 74 68 6F 64 F1 6C 61  6D 62 64 61 24 70 72 6F ethod·la mbda$pro
00000540 63 65 73 73 24 34 37 C4  66 69 6C 65 F6 45 6E 67 cess$47· file·Eng
00000550 69 6E 65 57 69 72 65 48  61 6E 64 6C 65 72 2E 6A ineWireH andler.j
00000560 61 76 61 C4 6C 69 6E 65  A1 9F 82 76 00 00 00 C5 ava·line ···v····
00000570 63 6C 61 73 73 B8 53 6E  65 74 2E 6F 70 65 6E 68 class·Sn et.openh
00000580 66 74 2E 63 68 72 6F 6E  69 63 6C 65 2E 65 6E 67 ft.chron icle.eng
00000590 69 6E 65 2E 73 65 72 76  65 72 2E 69 6E 74 65 72 ine.serv er.inter
000005a0 6E 61 6C 2E 45 6E 67 69  6E 65 57 69 72 65 48 61 nal.Engi neWireHa
000005b0 6E 64 6C 65 72 24 24 4C  61 6D 62 64 61 24 32 37 ndler$$L ambda$27
000005c0 2F 31 35 34 30 37 34 35  37 32 C6 6D 65 74 68 6F /1540745 72·metho
000005d0 64 E6 61 63 63 65 70 74  C4 66 69 6C 65 BB C4 6C d·accept ·file··l
000005e0 69 6E 65 A4 FF 82 57 00  00 00 C5 63 6C 61 73 73 ine···W· ···class
000005f0 B8 20 6E 65 74 2E 6F 70  65 6E 68 66 74 2E 63 68 · net.op enhft.ch
00000600 72 6F 6E 69 63 6C 65 2E  77 69 72 65 2E 57 69 72 ronicle. wire.Wir
00000610 65 73 C6 6D 65 74 68 6F  64 F1 6C 61 6D 62 64 61 es·metho d·lambda
00000620 24 72 65 61 64 44 61 74  61 24 32 C4 66 69 6C 65 $readDat a$2·file
00000630 EA 57 69 72 65 73 2E 6A  61 76 61 C4 6C 69 6E 65 ·Wires.j ava·line
00000640 78 82 59 00 00 00 C5 63  6C 61 73 73 B8 36 6E 65 x·Y····c lass·6ne
00000650 74 2E 6F 70 65 6E 68 66  74 2E 63 68 72 6F 6E 69 t.openhf t.chroni
00000660 63 6C 65 2E 77 69 72 65  2E 57 69 72 65 73 24 24 cle.wire .Wires$$
00000670 4C 61 6D 62 64 61 24 35  38 2F 31 39 33 31 36 32 Lambda$5 8/193162
00000680 35 31 31 39 C6 6D 65 74  68 6F 64 E6 61 63 63 65 5119·met hod·acce
00000690 70 74 C4 66 69 6C 65 BB  C4 6C 69 6E 65 A4 FF 82 pt·file· ·line···
000006a0 65 00 00 00 C5 63 6C 61  73 73 B8 2B 6E 65 74 2E e····cla ss·+net.
000006b0 6F 70 65 6E 68 66 74 2E  63 68 72 6F 6E 69 63 6C openhft. chronicl
000006c0 65 2E 62 79 74 65 73 2E  53 74 72 65 61 6D 69 6E e.bytes. Streamin
000006d0 67 43 6F 6D 6D 6F 6E C6  6D 65 74 68 6F 64 EA 77 gCommon· method·w
000006e0 69 74 68 4C 65 6E 67 74  68 C4 66 69 6C 65 F4 53 ithLengt h·file·S
000006f0 74 72 65 61 6D 69 6E 67  43 6F 6D 6D 6F 6E 2E 6A treaming Common.j
00000700 61 76 61 C4 6C 69 6E 65  34 82 4E 00 00 00 C5 63 ava·line 4·N····c
00000710 6C 61 73 73 B8 20 6E 65  74 2E 6F 70 65 6E 68 66 lass· ne t.openhf
00000720 74 2E 63 68 72 6F 6E 69  63 6C 65 2E 77 69 72 65 t.chroni cle.wire
00000730 2E 57 69 72 65 73 C6 6D  65 74 68 6F 64 E8 72 65 .Wires·m ethod·re
00000740 61 64 44 61 74 61 C4 66  69 6C 65 EA 57 69 72 65 adData·f ile·Wire
00000750 73 2E 6A 61 76 61 C4 6C  69 6E 65 78 82 54 00 00 s.java·l inex·T··
00000760 00 C5 63 6C 61 73 73 B8  21 6E 65 74 2E 6F 70 65 ··class· !net.ope
00000770 6E 68 66 74 2E 63 68 72  6F 6E 69 63 6C 65 2E 77 nhft.chr onicle.w
00000780 69 72 65 2E 57 69 72 65  49 6E C6 6D 65 74 68 6F ire.Wire In·metho
00000790 64 EC 72 65 61 64 44 6F  63 75 6D 65 6E 74 C4 66 d·readDo cument·f
000007a0 69 6C 65 EB 57 69 72 65  49 6E 2E 6A 61 76 61 C4 ile·Wire In.java·
000007b0 6C 69 6E 65 4B 82 78 00  00 00 C5 63 6C 61 73 73 lineK·x· ···class
000007c0 B8 3E 6E 65 74 2E 6F 70  65 6E 68 66 74 2E 63 68 ·>net.op enhft.ch
000007d0 72 6F 6E 69 63 6C 65 2E  65 6E 67 69 6E 65 2E 73 ronicle. engine.s
000007e0 65 72 76 65 72 2E 69 6E  74 65 72 6E 61 6C 2E 45 erver.in ternal.E
000007f0 6E 67 69 6E 65 57 69 72  65 48 61 6E 64 6C 65 72 ngineWir eHandler
00000800 C6 6D 65 74 68 6F 64 E7  70 72 6F 63 65 73 73 C4 ·method· process·
00000810 66 69 6C 65 F6 45 6E 67  69 6E 65 57 69 72 65 48 file·Eng ineWireH
00000820 61 6E 64 6C 65 72 2E 6A  61 76 61 C4 6C 69 6E 65 andler.j ava·line
00000830 A1 99 82 5F 00 00 00 C5  63 6C 61 73 73 B8 2C 6E ···_···· class·,n
00000840 65 74 2E 6F 70 65 6E 68  66 74 2E 63 68 72 6F 6E et.openh ft.chron
00000850 69 63 6C 65 2E 6E 65 74  77 6F 72 6B 2E 57 69 72 icle.net work.Wir
00000860 65 54 63 70 48 61 6E 64  6C 65 72 C6 6D 65 74 68 eTcpHand ler·meth
00000870 6F 64 E4 72 65 61 64 C4  66 69 6C 65 F3 57 69 72 od·read· file·Wir
00000880 65 54 63 70 48 61 6E 64  6C 65 72 2E 6A 61 76 61 eTcpHand ler.java
00000890 C4 6C 69 6E 65 64 82 62  00 00 00 C5 63 6C 61 73 ·lined·b ····clas
000008a0 73 B8 2C 6E 65 74 2E 6F  70 65 6E 68 66 74 2E 63 s·,net.o penhft.c
000008b0 68 72 6F 6E 69 63 6C 65  2E 6E 65 74 77 6F 72 6B hronicle .network
000008c0 2E 57 69 72 65 54 63 70  48 61 6E 64 6C 65 72 C6 .WireTcp Handler·
000008d0 6D 65 74 68 6F 64 E7 70  72 6F 63 65 73 73 C4 66 method·p rocess·f
000008e0 69 6C 65 F3 57 69 72 65  54 63 70 48 61 6E 64 6C ile·Wire TcpHandl
000008f0 65 72 2E 6A 61 76 61 C4  6C 69 6E 65 3D 82 6A 00 er.java· line=·j·
00000900 00 00 C5 63 6C 61 73 73  B8 2D 6E 65 74 2E 6F 70 ···class ·-net.op
00000910 65 6E 68 66 74 2E 63 68  72 6F 6E 69 63 6C 65 2E enhft.ch ronicle.
00000920 6E 65 74 77 6F 72 6B 2E  54 63 70 45 76 65 6E 74 network. TcpEvent
00000930 48 61 6E 64 6C 65 72 C6  6D 65 74 68 6F 64 ED 69 Handler· method·i
00000940 6E 76 6F 6B 65 48 61 6E  64 6C 65 72 C4 66 69 6C nvokeHan dler·fil
00000950 65 F4 54 63 70 45 76 65  6E 74 48 61 6E 64 6C 65 e·TcpEve ntHandle
00000960 72 2E 6A 61 76 61 C4 6C  69 6E 65 5B 82 64 00 00 r.java·l ine[·d··
00000970 00 C5 63 6C 61 73 73 B8  2D 6E 65 74 2E 6F 70 65 ··class· -net.ope
00000980 6E 68 66 74 2E 63 68 72  6F 6E 69 63 6C 65 2E 6E nhft.chr onicle.n
00000990 65 74 77 6F 72 6B 2E 54  63 70 45 76 65 6E 74 48 etwork.T cpEventH
000009a0 61 6E 64 6C 65 72 C6 6D  65 74 68 6F 64 E7 72 75 andler·m ethod·ru
000009b0 6E 4F 6E 63 65 C4 66 69  6C 65 F4 54 63 70 45 76 nOnce·fi le·TcpEv
000009c0 65 6E 74 48 61 6E 64 6C  65 72 2E 6A 61 76 61 C4 entHandl er.java·
000009d0 6C 69 6E 65 4F 82 77 00  00 00 C5 63 6C 61 73 73 lineO·w· ···class
000009e0 B8 34 6E 65 74 2E 6F 70  65 6E 68 66 74 2E 63 68 ·4net.op enhft.ch
000009f0 72 6F 6E 69 63 6C 65 2E  6E 65 74 77 6F 72 6B 2E ronicle. network.
00000a00 65 76 65 6E 74 2E 56 61  6E 69 6C 6C 61 45 76 65 event.Va nillaEve
00000a10 6E 74 4C 6F 6F 70 C6 6D  65 74 68 6F 64 F2 72 75 ntLoop·m ethod·ru
00000a20 6E 41 6C 6C 48 69 67 68  48 61 6E 64 6C 65 72 73 nAllHigh Handlers
00000a30 C4 66 69 6C 65 F5 56 61  6E 69 6C 6C 61 45 76 65 ·file·Va nillaEve
00000a40 6E 74 4C 6F 6F 70 2E 6A  61 76 61 C4 6C 69 6E 65 ntLoop.j ava·line
00000a50 7D 82 68 00 00 00 C5 63  6C 61 73 73 B8 34 6E 65 }·h····c lass·4ne
00000a60 74 2E 6F 70 65 6E 68 66  74 2E 63 68 72 6F 6E 69 t.openhf t.chroni
00000a70 63 6C 65 2E 6E 65 74 77  6F 72 6B 2E 65 76 65 6E cle.netw ork.even
00000a80 74 2E 56 61 6E 69 6C 6C  61 45 76 65 6E 74 4C 6F t.Vanill aEventLo
00000a90 6F 70 C6 6D 65 74 68 6F  64 E3 72 75 6E C4 66 69 op·metho d·run·fi
00000aa0 6C 65 F5 56 61 6E 69 6C  6C 61 45 76 65 6E 74 4C le·Vanil laEventL
00000ab0 6F 6F 70 2E 6A 61 76 61  C4 6C 69 6E 65 5F       oop.java ·line_  
```

### Entry Set
example of getting and entry set itterator

sends:

```yaml
00000000 23 00 00 40 B9 03 63 73  70 EF 2F 2F 74 65 73 74 #··@··cs p·//test
00000010 3F 76 69 65 77 3D 4D 41  50 B9 03 74 69 64 A7 5F ?view=MA P··tid·_
00000020 F9 46 AF 4D 01 00 00 0F  00 00 00 B9 08 65 6E 74 ·F·M···· ·····ent
00000030 72 79 53 65 74 82 00 00  00 00                   rySet··· ··      
```

receives:

```yaml
00000000 37 00 00 00 B9 05 72 65  70 6C 79 B6 09 73 65 74 7·····re ply··set
00000010 2D 70 72 6F 78 79 82 20  00 00 00 B9 03 63 73 70 -proxy·  ·····csp
00000020 F4 2F 2F 74 65 73 74 3F  76 69 65 77 3D 65 6E 74 ·//test? view=ent
00000030 72 79 53 65 74 B9 03 63  69 64 01                rySet··c id·     
```

sends:

```yaml
00000000 14 00 00 40 B9 03 63 69  64 01 B9 03 74 69 64 A7 ···@··ci d···tid·
00000010 66 F9 46 AF 4D 01 00 00  17 00 00 00 B9 10 6E 75 f·F·M··· ······nu
00000020 6D 62 65 72 4F 66 53 65  67 6D 65 6E 74 73 82 00 mberOfSe gments··
00000030 00 00 00                                         ···              
```

receives:

```yaml
00000000 07 00 00 00 C5 72 65 70  6C 79 01                ·····rep ly·     
```

sends:

```yaml
00000000 14 00 00 40 B9 03 63 69  64 01 B9 03 74 69 64 A7 ···@··ci d···tid·
00000010 6A F9 46 AF 4D 01 00 00  0B 00 00 00 B9 08 69 74 j·F·M··· ······it
00000020 65 72 61 74 6F 72 01                             erator·          
```

receives:

```yaml
00000000 6B 00 00 00 B9 05 72 65  70 6C 79 82 5F 00 00 00 k·····re ply·_···
00000010 82 0E 00 00 00 C3 6B 65  79 E1 34 C5 76 61 6C 75 ······ke y·4·valu
00000020 65 E1 44 82 0E 00 00 00  C3 6B 65 79 E1 35 C5 76 e·D····· ·key·5·v
00000030 61 6C 75 65 E1 45 82 0E  00 00 00 C3 6B 65 79 E1 alue·E·· ····key·
00000040 32 C5 76 61 6C 75 65 E1  42 82 0E 00 00 00 C3 6B 2·value· B······k
00000050 65 79 E1 33 C5 76 61 6C  75 65 E1 43 82 0E 00 00 ey·3·val ue·C····
00000060 00 C3 6B 65 79 E1 31 C5  76 61 6C 75 65 E1 41    ··key·1· value·A 
```

### Replace Value 2
example of replace where the value is known

sends:

```yaml
00000000 23 00 00 40 B9 03 63 73  70 EF 2F 2F 74 65 73 74 #··@··cs p·//test
00000010 3F 76 69 65 77 3D 4D 41  50 B9 03 74 69 64 A7 DE ?view=MA P··tid··
00000020 0A 47 AF 4D 01 00 00 2F  00 00 00 B9 0D 72 65 70 ·G·M···/ ·····rep
00000030 6C 61 63 65 46 6F 72 4F  6C 64 82 1B 00 00 00 C3 laceForO ld······
00000040 6B 65 79 01 C8 6F 6C 64  56 61 6C 75 65 E1 41 C8 key··old Value·A·
00000050 6E 65 77 56 61 6C 75 65  E1 5A                   newValue ·Z      
```

receives:

```yaml
00000000 08 00 00 00 B9 05 72 65  70 6C 79 B1             ······re ply·    
```

### Clear
sends:

```yaml
00000000 23 00 00 40 B9 03 63 73  70 EF 2F 2F 74 65 73 74 #··@··cs p·//test
00000010 3F 76 69 65 77 3D 4D 41  50 B9 03 74 69 64 A7 98 ?view=MA P··tid··
00000020 13 47 AF 4D 01 00 00 0C  00 00 00 B9 05 63 6C 65 ·G·M···· ·····cle
00000030 61 72 82 00 00 00 00                             ar·····          
```

receives:

```yaml
00000000 0C 00 00 00 B9 05 72 65  70 6C 79 82 00 00 00 00 ······re ply·····
```

### Size
size on an empty map

sends:

```yaml
00000000 23 00 00 40 B9 03 63 73  70 EF 2F 2F 74 65 73 74 #··@··cs p·//test
00000010 3F 76 69 65 77 3D 4D 41  50 B9 03 74 69 64 A7 7F ?view=MA P··tid··
00000020 3D 47 AF 4D 01 00 00 0B  00 00 00 B9 04 73 69 7A =G·M···· ·····siz
00000030 65 82 00 00 00 00                                e·····           
```

receives:

```yaml
00000000 08 00 00 00 B9 05 72 65  70 6C 79 00             ······re ply·    
```

size on a map with entries

sends:

```yaml
00000000 23 00 00 40 B9 03 63 73  70 EF 2F 2F 74 65 73 74 #··@··cs p·//test
00000010 3F 76 69 65 77 3D 4D 41  50 B9 03 74 69 64 A7 81 ?view=MA P··tid··
00000020 3D 47 AF 4D 01 00 00 0B  00 00 00 B9 04 73 69 7A =G·M···· ·····siz
00000030 65 82 00 00 00 00                                e·····           
```

receives:

```yaml
00000000 08 00 00 00 B9 05 72 65  70 6C 79 05             ······re ply·    
```

### Contains Key
example of containsKey(<key>) returning true

sends:

```yaml
00000000 23 00 00 40 B9 03 63 73  70 EF 2F 2F 74 65 73 74 #··@··cs p·//test
00000010 3F 76 69 65 77 3D 4D 41  50 B9 03 74 69 64 A7 C6 ?view=MA P··tid··
00000020 56 47 AF 4D 01 00 00 0E  00 00 00 B9 0B 63 6F 6E VG·M···· ·····con
00000030 74 61 69 6E 73 4B 65 79  01                      tainsKey ·       
```

receives:

```yaml
00000000 08 00 00 00 B9 05 72 65  70 6C 79 B1             ······re ply·    
```

### Put If Absent
sends:

```yaml
00000000 23 00 00 40 B9 03 63 73  70 EF 2F 2F 74 65 73 74 #··@··cs p·//test
00000010 3F 76 69 65 77 3D 4D 41  50 B9 03 74 69 64 A7 81 ?view=MA P··tid··
00000020 5F 47 AF 4D 01 00 00 1F  00 00 00 B9 0B 70 75 74 _G·M···· ·····put
00000030 49 66 41 62 73 65 6E 74  82 0D 00 00 00 C3 6B 65 IfAbsent ······ke
00000040 79 06 C5 76 61 6C 75 65  E1 5A                   y··value ·Z      
```

receives:

```yaml
00000000 08 00 00 00 B9 05 72 65  70 6C 79 BB             ······re ply·    
```

### Contains Value
example of containsValue(<value>) returning true

sends:

```yaml
00000000 23 00 00 40 B9 03 63 73  70 EF 2F 2F 74 65 73 74 #··@··cs p·//test
00000010 3F 76 69 65 77 3D 4D 41  50 B9 03 74 69 64 A7 3D ?view=MA P··tid·=
00000020 68 47 AF 4D 01 00 00 11  00 00 00 B9 0D 63 6F 6E hG·M···· ·····con
00000030 74 61 69 6E 73 56 61 6C  75 65 E1 41             tainsVal ue·A    
```

receives:

```yaml
00000000 08 00 00 00 B9 05 72 65  70 6C 79 B1             ······re ply·    
```

### Contains
when the key exists

sends:

```yaml
00000000 23 00 00 40 B9 03 63 73  70 EF 2F 2F 74 65 73 74 #··@··cs p·//test
00000010 3F 76 69 65 77 3D 4D 41  50 B9 03 74 69 64 A7 F8 ?view=MA P··tid··
00000020 70 47 AF 4D 01 00 00 11  00 00 00 B9 0D 63 6F 6E pG·M···· ·····con
00000030 74 61 69 6E 73 56 61 6C  75 65 E1 41             tainsVal ue·A    
```

receives:

```yaml
00000000 08 00 00 00 B9 05 72 65  70 6C 79 B1             ······re ply·    
```

when it doesnt exist

sends:

```yaml
00000000 23 00 00 40 B9 03 63 73  70 EF 2F 2F 74 65 73 74 #··@··cs p·//test
00000010 3F 76 69 65 77 3D 4D 41  50 B9 03 74 69 64 A7 F9 ?view=MA P··tid··
00000020 70 47 AF 4D 01 00 00 11  00 00 00 B9 0D 63 6F 6E pG·M···· ·····con
00000030 74 61 69 6E 73 56 61 6C  75 65 E1 5A             tainsVal ue·Z    
```

receives:

```yaml
00000000 08 00 00 00 B9 05 72 65  70 6C 79 B0             ······re ply·    
```

### Replace 2
example of replace where the value is known

sends:

```yaml
00000000 23 00 00 40 B9 03 63 73  70 EF 2F 2F 74 65 73 74 #··@··cs p·//test
00000010 3F 76 69 65 77 3D 4D 41  50 B9 03 74 69 64 A7 B5 ?view=MA P··tid··
00000020 79 47 AF 4D 01 00 00 1B  00 00 00 B9 07 72 65 70 yG·M···· ·····rep
00000030 6C 61 63 65 82 0D 00 00  00 C3 6B 65 79 01 C5 76 lace···· ··key··v
00000040 61 6C 75 65 E1 5A                                alue·Z           
```

receives:

```yaml
00000000 09 00 00 00 B9 05 72 65  70 6C 79 E1 41          ······re ply·A   
```

### Put If Absent 2
replace(notPresent, "A", null will throw a NullPointerException

sends:

```yaml
00000000 23 00 00 40 B9 03 63 73  70 EF 2F 2F 74 65 73 74 #··@··cs p·//test
00000010 3F 76 69 65 77 3D 4D 41  50 B9 03 74 69 64 A7 33 ?view=MA P··tid·3
00000020 8B 47 AF 4D 01 00 00 1F  00 00 00 B9 0B 70 75 74 ·G·M···· ·····put
00000030 49 66 41 62 73 65 6E 74  82 0D 00 00 00 C3 6B 65 IfAbsent ······ke
00000040 79 01 C5 76 61 6C 75 65  E1 5A                   y··value ·Z      
```

receives:

```yaml
00000000 09 00 00 00 B9 05 72 65  70 6C 79 E1 41          ······re ply·A   
```

### Replace
example of replace where the value is not known

sends:

```yaml
00000000 23 00 00 40 B9 03 63 73  70 EF 2F 2F 74 65 73 74 #··@··cs p·//test
00000010 3F 76 69 65 77 3D 4D 41  50 B9 03 74 69 64 A7 A2 ?view=MA P··tid··
00000020 AE 47 AF 4D 01 00 00 1B  00 00 00 B9 07 72 65 70 ·G·M···· ·····rep
00000030 6C 61 63 65 82 0D 00 00  00 C3 6B 65 79 06 C5 76 lace···· ··key··v
00000040 61 6C 75 65 E1 5A                                alue·Z           
```

receives:

```yaml
00000000 08 00 00 00 B9 05 72 65  70 6C 79 BB             ······re ply·    
```

### Get _ Null Pointer Exception
get(null) returns a NullPointerException

sends:

```yaml
00000000 23 00 00 40 B9 03 63 73  70 EF 2F 2F 74 65 73 74 #··@··cs p·//test
00000010 3F 76 69 65 77 3D 4D 41  50 B9 03 74 69 64 A7 13 ?view=MA P··tid··
00000020 C0 47 AF 4D 01 00 00 06  00 00 00 B9 03 67 65 74 ·G·M···· ·····get
00000030 BB                                               ·                
```

receives:

```yaml
00000000 BB 0A 00 00 B9 09 65 78  63 65 70 74 69 6F 6E B6 ······ex ception·
00000010 1E 6A 61 76 61 2E 6C 61  6E 67 2E 4E 75 6C 6C 50 ·java.la ng.NullP
00000020 6F 69 6E 74 65 72 45 78  63 65 70 74 69 6F 6E 82 ointerEx ception·
00000030 8B 0A 00 00 C7 6D 65 73  73 61 67 65 BB CA 73 74 ·····mes sage··st
00000040 61 63 6B 54 72 61 63 65  82 72 0A 00 00 82 69 00 ackTrace ·r····i·
00000050 00 00 C5 63 6C 61 73 73  B8 2F 6E 65 74 2E 6F 70 ···class ·/net.op
00000060 65 6E 68 66 74 2E 63 68  72 6F 6E 69 63 6C 65 2E enhft.ch ronicle.
00000070 65 6E 67 69 6E 65 2E 6D  61 70 2E 4D 61 70 57 69 engine.m ap.MapWi
00000080 72 65 48 61 6E 64 6C 65  72 C6 6D 65 74 68 6F 64 reHandle r·method
00000090 E9 6E 75 6C 6C 43 68 65  63 6B C4 66 69 6C 65 F3 ·nullChe ck·file·
000000a0 4D 61 70 57 69 72 65 48  61 6E 64 6C 65 72 2E 6A MapWireH andler.j
000000b0 61 76 61 C4 6C 69 6E 65  A2 85 01 82 72 00 00 00 ava·line ····r···
000000c0 C5 63 6C 61 73 73 B8 31  6E 65 74 2E 6F 70 65 6E ·class·1 net.open
000000d0 68 66 74 2E 63 68 72 6F  6E 69 63 6C 65 2E 65 6E hft.chro nicle.en
000000e0 67 69 6E 65 2E 6D 61 70  2E 4D 61 70 57 69 72 65 gine.map .MapWire
000000f0 48 61 6E 64 6C 65 72 24  31 C6 6D 65 74 68 6F 64 Handler$ 1·method
00000100 F0 6C 61 6D 62 64 61 24  61 63 63 65 70 74 24 32 ·lambda$ accept$2
00000110 32 C4 66 69 6C 65 F3 4D  61 70 57 69 72 65 48 61 2·file·M apWireHa
00000120 6E 64 6C 65 72 2E 6A 61  76 61 C4 6C 69 6E 65 A2 ndler.ja va·line·
00000130 0C 01 82 69 00 00 00 C5  63 6C 61 73 73 B8 46 6E ···i···· class·Fn
00000140 65 74 2E 6F 70 65 6E 68  66 74 2E 63 68 72 6F 6E et.openh ft.chron
00000150 69 63 6C 65 2E 65 6E 67  69 6E 65 2E 6D 61 70 2E icle.eng ine.map.
00000160 4D 61 70 57 69 72 65 48  61 6E 64 6C 65 72 24 31 MapWireH andler$1
00000170 24 24 4C 61 6D 62 64 61  24 36 35 2F 37 38 31 34 $$Lambda $65/7814
00000180 34 35 37 37 30 C6 6D 65  74 68 6F 64 E6 61 63 63 45770·me thod·acc
00000190 65 70 74 C4 66 69 6C 65  BB C4 6C 69 6E 65 A4 FF ept·file ··line··
000001a0 82 73 00 00 00 C5 63 6C  61 73 73 B8 2F 6E 65 74 ·s····cl ass·/net
000001b0 2E 6F 70 65 6E 68 66 74  2E 63 68 72 6F 6E 69 63 .openhft .chronic
000001c0 6C 65 2E 65 6E 67 69 6E  65 2E 6D 61 70 2E 4D 61 le.engin e.map.Ma
000001d0 70 57 69 72 65 48 61 6E  64 6C 65 72 C6 6D 65 74 pWireHan dler·met
000001e0 68 6F 64 F3 6C 61 6D 62  64 61 24 77 72 69 74 65 hod·lamb da$write
000001f0 44 61 74 61 24 32 35 C4  66 69 6C 65 F3 4D 61 70 Data$25· file·Map
00000200 57 69 72 65 48 61 6E 64  6C 65 72 2E 6A 61 76 61 WireHand ler.java
00000210 C4 6C 69 6E 65 A2 9D 01  82 67 00 00 00 C5 63 6C ·line··· ·g····cl
00000220 61 73 73 B8 44 6E 65 74  2E 6F 70 65 6E 68 66 74 ass·Dnet .openhft
00000230 2E 63 68 72 6F 6E 69 63  6C 65 2E 65 6E 67 69 6E .chronic le.engin
00000240 65 2E 6D 61 70 2E 4D 61  70 57 69 72 65 48 61 6E e.map.Ma pWireHan
00000250 64 6C 65 72 24 24 4C 61  6D 62 64 61 24 36 36 2F dler$$La mbda$66/
00000260 35 31 34 34 31 32 35 32  33 C6 6D 65 74 68 6F 64 51441252 3·method
00000270 E6 61 63 63 65 70 74 C4  66 69 6C 65 BB C4 6C 69 ·accept· file··li
00000280 6E 65 A4 FF 82 4F 00 00  00 C5 63 6C 61 73 73 B8 ne···O·· ··class·
00000290 20 6E 65 74 2E 6F 70 65  6E 68 66 74 2E 63 68 72  net.ope nhft.chr
000002a0 6F 6E 69 63 6C 65 2E 77  69 72 65 2E 57 69 72 65 onicle.w ire.Wire
000002b0 73 C6 6D 65 74 68 6F 64  E9 77 72 69 74 65 44 61 s·method ·writeDa
000002c0 74 61 C4 66 69 6C 65 EA  57 69 72 65 73 2E 6A 61 ta·file· Wires.ja
000002d0 76 61 C4 6C 69 6E 65 4E  82 57 00 00 00 C5 63 6C va·lineN ·W····cl
000002e0 61 73 73 B8 22 6E 65 74  2E 6F 70 65 6E 68 66 74 ass·"net .openhft
000002f0 2E 63 68 72 6F 6E 69 63  6C 65 2E 77 69 72 65 2E .chronic le.wire.
00000300 57 69 72 65 4F 75 74 C6  6D 65 74 68 6F 64 ED 77 WireOut· method·w
00000310 72 69 74 65 44 6F 63 75  6D 65 6E 74 C4 66 69 6C riteDocu ment·fil
00000320 65 EC 57 69 72 65 4F 75  74 2E 6A 61 76 61 C4 6C e·WireOu t.java·l
00000330 69 6E 65 44 82 69 00 00  00 C5 63 6C 61 73 73 B8 ineD·i·· ··class·
00000340 2F 6E 65 74 2E 6F 70 65  6E 68 66 74 2E 63 68 72 /net.ope nhft.chr
00000350 6F 6E 69 63 6C 65 2E 65  6E 67 69 6E 65 2E 6D 61 onicle.e ngine.ma
00000360 70 2E 4D 61 70 57 69 72  65 48 61 6E 64 6C 65 72 p.MapWir eHandler
00000370 C6 6D 65 74 68 6F 64 E9  77 72 69 74 65 44 61 74 ·method· writeDat
00000380 61 C4 66 69 6C 65 F3 4D  61 70 57 69 72 65 48 61 a·file·M apWireHa
00000390 6E 64 6C 65 72 2E 6A 61  76 61 C4 6C 69 6E 65 A2 ndler.ja va·line·
000003a0 99 01 82 67 00 00 00 C5  63 6C 61 73 73 B8 31 6E ···g···· class·1n
000003b0 65 74 2E 6F 70 65 6E 68  66 74 2E 63 68 72 6F 6E et.openh ft.chron
000003c0 69 63 6C 65 2E 65 6E 67  69 6E 65 2E 6D 61 70 2E icle.eng ine.map.
000003d0 4D 61 70 57 69 72 65 48  61 6E 64 6C 65 72 24 31 MapWireH andler$1
000003e0 C6 6D 65 74 68 6F 64 E6  61 63 63 65 70 74 C4 66 ·method· accept·f
000003f0 69 6C 65 F3 4D 61 70 57  69 72 65 48 61 6E 64 6C ile·MapW ireHandl
00000400 65 72 2E 6A 61 76 61 C4  6C 69 6E 65 A1 C9 82 67 er.java· line···g
00000410 00 00 00 C5 63 6C 61 73  73 B8 31 6E 65 74 2E 6F ····clas s·1net.o
00000420 70 65 6E 68 66 74 2E 63  68 72 6F 6E 69 63 6C 65 penhft.c hronicle
00000430 2E 65 6E 67 69 6E 65 2E  6D 61 70 2E 4D 61 70 57 .engine. map.MapW
00000440 69 72 65 48 61 6E 64 6C  65 72 24 31 C6 6D 65 74 ireHandl er$1·met
00000450 68 6F 64 E6 61 63 63 65  70 74 C4 66 69 6C 65 F3 hod·acce pt·file·
00000460 4D 61 70 57 69 72 65 48  61 6E 64 6C 65 72 2E 6A MapWireH andler.j
00000470 61 76 61 C4 6C 69 6E 65  A1 AD 82 65 00 00 00 C5 ava·line ···e····
00000480 63 6C 61 73 73 B8 2F 6E  65 74 2E 6F 70 65 6E 68 class·/n et.openh
00000490 66 74 2E 63 68 72 6F 6E  69 63 6C 65 2E 65 6E 67 ft.chron icle.eng
000004a0 69 6E 65 2E 6D 61 70 2E  4D 61 70 57 69 72 65 48 ine.map. MapWireH
000004b0 61 6E 64 6C 65 72 C6 6D  65 74 68 6F 64 E7 70 72 andler·m ethod·pr
000004c0 6F 63 65 73 73 C4 66 69  6C 65 F3 4D 61 70 57 69 ocess·fi le·MapWi
000004d0 72 65 48 61 6E 64 6C 65  72 2E 6A 61 76 61 C4 6C reHandle r.java·l
000004e0 69 6E 65 4E 82 82 00 00  00 C5 63 6C 61 73 73 B8 ineN···· ··class·
000004f0 3E 6E 65 74 2E 6F 70 65  6E 68 66 74 2E 63 68 72 >net.ope nhft.chr
00000500 6F 6E 69 63 6C 65 2E 65  6E 67 69 6E 65 2E 73 65 onicle.e ngine.se
00000510 72 76 65 72 2E 69 6E 74  65 72 6E 61 6C 2E 45 6E rver.int ernal.En
00000520 67 69 6E 65 57 69 72 65  48 61 6E 64 6C 65 72 C6 gineWire Handler·
00000530 6D 65 74 68 6F 64 F1 6C  61 6D 62 64 61 24 70 72 method·l ambda$pr
00000540 6F 63 65 73 73 24 34 37  C4 66 69 6C 65 F6 45 6E ocess$47 ·file·En
00000550 67 69 6E 65 57 69 72 65  48 61 6E 64 6C 65 72 2E gineWire Handler.
00000560 6A 61 76 61 C4 6C 69 6E  65 A1 9F 82 76 00 00 00 java·lin e···v···
00000570 C5 63 6C 61 73 73 B8 53  6E 65 74 2E 6F 70 65 6E ·class·S net.open
00000580 68 66 74 2E 63 68 72 6F  6E 69 63 6C 65 2E 65 6E hft.chro nicle.en
00000590 67 69 6E 65 2E 73 65 72  76 65 72 2E 69 6E 74 65 gine.ser ver.inte
000005a0 72 6E 61 6C 2E 45 6E 67  69 6E 65 57 69 72 65 48 rnal.Eng ineWireH
000005b0 61 6E 64 6C 65 72 24 24  4C 61 6D 62 64 61 24 32 andler$$ Lambda$2
000005c0 37 2F 31 35 34 30 37 34  35 37 32 C6 6D 65 74 68 7/154074 572·meth
000005d0 6F 64 E6 61 63 63 65 70  74 C4 66 69 6C 65 BB C4 od·accep t·file··
000005e0 6C 69 6E 65 A4 FF 82 57  00 00 00 C5 63 6C 61 73 line···W ····clas
000005f0 73 B8 20 6E 65 74 2E 6F  70 65 6E 68 66 74 2E 63 s· net.o penhft.c
00000600 68 72 6F 6E 69 63 6C 65  2E 77 69 72 65 2E 57 69 hronicle .wire.Wi
00000610 72 65 73 C6 6D 65 74 68  6F 64 F1 6C 61 6D 62 64 res·meth od·lambd
00000620 61 24 72 65 61 64 44 61  74 61 24 32 C4 66 69 6C a$readDa ta$2·fil
00000630 65 EA 57 69 72 65 73 2E  6A 61 76 61 C4 6C 69 6E e·Wires. java·lin
00000640 65 78 82 59 00 00 00 C5  63 6C 61 73 73 B8 36 6E ex·Y···· class·6n
00000650 65 74 2E 6F 70 65 6E 68  66 74 2E 63 68 72 6F 6E et.openh ft.chron
00000660 69 63 6C 65 2E 77 69 72  65 2E 57 69 72 65 73 24 icle.wir e.Wires$
00000670 24 4C 61 6D 62 64 61 24  35 38 2F 31 39 33 31 36 $Lambda$ 58/19316
00000680 32 35 31 31 39 C6 6D 65  74 68 6F 64 E6 61 63 63 25119·me thod·acc
00000690 65 70 74 C4 66 69 6C 65  BB C4 6C 69 6E 65 A4 FF ept·file ··line··
000006a0 82 65 00 00 00 C5 63 6C  61 73 73 B8 2B 6E 65 74 ·e····cl ass·+net
000006b0 2E 6F 70 65 6E 68 66 74  2E 63 68 72 6F 6E 69 63 .openhft .chronic
000006c0 6C 65 2E 62 79 74 65 73  2E 53 74 72 65 61 6D 69 le.bytes .Streami
000006d0 6E 67 43 6F 6D 6D 6F 6E  C6 6D 65 74 68 6F 64 EA ngCommon ·method·
000006e0 77 69 74 68 4C 65 6E 67  74 68 C4 66 69 6C 65 F4 withLeng th·file·
000006f0 53 74 72 65 61 6D 69 6E  67 43 6F 6D 6D 6F 6E 2E Streamin gCommon.
00000700 6A 61 76 61 C4 6C 69 6E  65 34 82 4E 00 00 00 C5 java·lin e4·N····
00000710 63 6C 61 73 73 B8 20 6E  65 74 2E 6F 70 65 6E 68 class· n et.openh
00000720 66 74 2E 63 68 72 6F 6E  69 63 6C 65 2E 77 69 72 ft.chron icle.wir
00000730 65 2E 57 69 72 65 73 C6  6D 65 74 68 6F 64 E8 72 e.Wires· method·r
00000740 65 61 64 44 61 74 61 C4  66 69 6C 65 EA 57 69 72 eadData· file·Wir
00000750 65 73 2E 6A 61 76 61 C4  6C 69 6E 65 78 82 54 00 es.java· linex·T·
00000760 00 00 C5 63 6C 61 73 73  B8 21 6E 65 74 2E 6F 70 ···class ·!net.op
00000770 65 6E 68 66 74 2E 63 68  72 6F 6E 69 63 6C 65 2E enhft.ch ronicle.
00000780 77 69 72 65 2E 57 69 72  65 49 6E C6 6D 65 74 68 wire.Wir eIn·meth
00000790 6F 64 EC 72 65 61 64 44  6F 63 75 6D 65 6E 74 C4 od·readD ocument·
000007a0 66 69 6C 65 EB 57 69 72  65 49 6E 2E 6A 61 76 61 file·Wir eIn.java
000007b0 C4 6C 69 6E 65 4B 82 78  00 00 00 C5 63 6C 61 73 ·lineK·x ····clas
000007c0 73 B8 3E 6E 65 74 2E 6F  70 65 6E 68 66 74 2E 63 s·>net.o penhft.c
000007d0 68 72 6F 6E 69 63 6C 65  2E 65 6E 67 69 6E 65 2E hronicle .engine.
000007e0 73 65 72 76 65 72 2E 69  6E 74 65 72 6E 61 6C 2E server.i nternal.
000007f0 45 6E 67 69 6E 65 57 69  72 65 48 61 6E 64 6C 65 EngineWi reHandle
00000800 72 C6 6D 65 74 68 6F 64  E7 70 72 6F 63 65 73 73 r·method ·process
00000810 C4 66 69 6C 65 F6 45 6E  67 69 6E 65 57 69 72 65 ·file·En gineWire
00000820 48 61 6E 64 6C 65 72 2E  6A 61 76 61 C4 6C 69 6E Handler. java·lin
00000830 65 A1 99 82 5F 00 00 00  C5 63 6C 61 73 73 B8 2C e···_··· ·class·,
00000840 6E 65 74 2E 6F 70 65 6E  68 66 74 2E 63 68 72 6F net.open hft.chro
00000850 6E 69 63 6C 65 2E 6E 65  74 77 6F 72 6B 2E 57 69 nicle.ne twork.Wi
00000860 72 65 54 63 70 48 61 6E  64 6C 65 72 C6 6D 65 74 reTcpHan dler·met
00000870 68 6F 64 E4 72 65 61 64  C4 66 69 6C 65 F3 57 69 hod·read ·file·Wi
00000880 72 65 54 63 70 48 61 6E  64 6C 65 72 2E 6A 61 76 reTcpHan dler.jav
00000890 61 C4 6C 69 6E 65 64 82  62 00 00 00 C5 63 6C 61 a·lined· b····cla
000008a0 73 73 B8 2C 6E 65 74 2E  6F 70 65 6E 68 66 74 2E ss·,net. openhft.
000008b0 63 68 72 6F 6E 69 63 6C  65 2E 6E 65 74 77 6F 72 chronicl e.networ
000008c0 6B 2E 57 69 72 65 54 63  70 48 61 6E 64 6C 65 72 k.WireTc pHandler
000008d0 C6 6D 65 74 68 6F 64 E7  70 72 6F 63 65 73 73 C4 ·method· process·
000008e0 66 69 6C 65 F3 57 69 72  65 54 63 70 48 61 6E 64 file·Wir eTcpHand
000008f0 6C 65 72 2E 6A 61 76 61  C4 6C 69 6E 65 3D 82 6A ler.java ·line=·j
00000900 00 00 00 C5 63 6C 61 73  73 B8 2D 6E 65 74 2E 6F ····clas s·-net.o
00000910 70 65 6E 68 66 74 2E 63  68 72 6F 6E 69 63 6C 65 penhft.c hronicle
00000920 2E 6E 65 74 77 6F 72 6B  2E 54 63 70 45 76 65 6E .network .TcpEven
00000930 74 48 61 6E 64 6C 65 72  C6 6D 65 74 68 6F 64 ED tHandler ·method·
00000940 69 6E 76 6F 6B 65 48 61  6E 64 6C 65 72 C4 66 69 invokeHa ndler·fi
00000950 6C 65 F4 54 63 70 45 76  65 6E 74 48 61 6E 64 6C le·TcpEv entHandl
00000960 65 72 2E 6A 61 76 61 C4  6C 69 6E 65 5B 82 64 00 er.java· line[·d·
00000970 00 00 C5 63 6C 61 73 73  B8 2D 6E 65 74 2E 6F 70 ···class ·-net.op
00000980 65 6E 68 66 74 2E 63 68  72 6F 6E 69 63 6C 65 2E enhft.ch ronicle.
00000990 6E 65 74 77 6F 72 6B 2E  54 63 70 45 76 65 6E 74 network. TcpEvent
000009a0 48 61 6E 64 6C 65 72 C6  6D 65 74 68 6F 64 E7 72 Handler· method·r
000009b0 75 6E 4F 6E 63 65 C4 66  69 6C 65 F4 54 63 70 45 unOnce·f ile·TcpE
000009c0 76 65 6E 74 48 61 6E 64  6C 65 72 2E 6A 61 76 61 ventHand ler.java
000009d0 C4 6C 69 6E 65 4F 82 77  00 00 00 C5 63 6C 61 73 ·lineO·w ····clas
000009e0 73 B8 34 6E 65 74 2E 6F  70 65 6E 68 66 74 2E 63 s·4net.o penhft.c
000009f0 68 72 6F 6E 69 63 6C 65  2E 6E 65 74 77 6F 72 6B hronicle .network
00000a00 2E 65 76 65 6E 74 2E 56  61 6E 69 6C 6C 61 45 76 .event.V anillaEv
00000a10 65 6E 74 4C 6F 6F 70 C6  6D 65 74 68 6F 64 F2 72 entLoop· method·r
00000a20 75 6E 41 6C 6C 48 69 67  68 48 61 6E 64 6C 65 72 unAllHig hHandler
00000a30 73 C4 66 69 6C 65 F5 56  61 6E 69 6C 6C 61 45 76 s·file·V anillaEv
00000a40 65 6E 74 4C 6F 6F 70 2E  6A 61 76 61 C4 6C 69 6E entLoop. java·lin
00000a50 65 7D 82 68 00 00 00 C5  63 6C 61 73 73 B8 34 6E e}·h···· class·4n
00000a60 65 74 2E 6F 70 65 6E 68  66 74 2E 63 68 72 6F 6E et.openh ft.chron
00000a70 69 63 6C 65 2E 6E 65 74  77 6F 72 6B 2E 65 76 65 icle.net work.eve
00000a80 6E 74 2E 56 61 6E 69 6C  6C 61 45 76 65 6E 74 4C nt.Vanil laEventL
00000a90 6F 6F 70 C6 6D 65 74 68  6F 64 E3 72 75 6E C4 66 oop·meth od·run·f
00000aa0 69 6C 65 F5 56 61 6E 69  6C 6C 61 45 76 65 6E 74 ile·Vani llaEvent
00000ab0 4C 6F 6F 70 2E 6A 61 76  61 C4 6C 69 6E 65 5F    Loop.jav a·line_ 
```

### Entry Set To Array
map.entrySet().toArray() first gets the entry set and then converts it to an array

sends:

```yaml
00000000 23 00 00 40 B9 03 63 73  70 EF 2F 2F 74 65 73 74 #··@··cs p·//test
00000010 3F 76 69 65 77 3D 4D 41  50 B9 03 74 69 64 A7 8F ?view=MA P··tid··
00000020 D1 47 AF 4D 01 00 00 0F  00 00 00 B9 08 65 6E 74 ·G·M···· ·····ent
00000030 72 79 53 65 74 82 00 00  00 00                   rySet··· ··      
```

receives:

```yaml
00000000 37 00 00 00 B9 05 72 65  70 6C 79 B6 09 73 65 74 7·····re ply··set
00000010 2D 70 72 6F 78 79 82 20  00 00 00 B9 03 63 73 70 -proxy·  ·····csp
00000020 F4 2F 2F 74 65 73 74 3F  76 69 65 77 3D 65 6E 74 ·//test? view=ent
00000030 72 79 53 65 74 B9 03 63  69 64 01                rySet··c id·     
```

sends:

```yaml
00000000 14 00 00 40 B9 03 63 69  64 01 B9 03 74 69 64 A7 ···@··ci d···tid·
00000010 90 D1 47 AF 4D 01 00 00  17 00 00 00 B9 10 6E 75 ··G·M··· ······nu
00000020 6D 62 65 72 4F 66 53 65  67 6D 65 6E 74 73 82 00 mberOfSe gments··
00000030 00 00 00                                         ···              
```

receives:

```yaml
00000000 07 00 00 00 C5 72 65 70  6C 79 01                ·····rep ly·     
```

sends:

```yaml
00000000 14 00 00 40 B9 03 63 69  64 01 B9 03 74 69 64 A7 ···@··ci d···tid·
00000010 93 D1 47 AF 4D 01 00 00  0B 00 00 00 B9 08 69 74 ··G·M··· ······it
00000020 65 72 61 74 6F 72 00                             erator·          
```

receives:

```yaml
00000000 6B 00 00 00 B9 05 72 65  70 6C 79 82 5F 00 00 00 k·····re ply·_···
00000010 82 0E 00 00 00 C3 6B 65  79 E1 34 C5 76 61 6C 75 ······ke y·4·valu
00000020 65 E1 44 82 0E 00 00 00  C3 6B 65 79 E1 35 C5 76 e·D····· ·key·5·v
00000030 61 6C 75 65 E1 45 82 0E  00 00 00 C3 6B 65 79 E1 alue·E·· ····key·
00000040 32 C5 76 61 6C 75 65 E1  42 82 0E 00 00 00 C3 6B 2·value· B······k
00000050 65 79 E1 33 C5 76 61 6C  75 65 E1 43 82 0E 00 00 ey·3·val ue·C····
00000060 00 C3 6B 65 79 E1 31 C5  76 61 6C 75 65 E1 41    ··key·1· value·A 
```

### Replace Value
example of when then value was not replaced

sends:

```yaml
00000000 23 00 00 40 B9 03 63 73  70 EF 2F 2F 74 65 73 74 #··@··cs p·//test
00000010 3F 76 69 65 77 3D 4D 41  50 B9 03 74 69 64 A7 C9 ?view=MA P··tid··
00000020 EB 47 AF 4D 01 00 00 2F  00 00 00 B9 0D 72 65 70 ·G·M···/ ·····rep
00000030 6C 61 63 65 46 6F 72 4F  6C 64 82 1B 00 00 00 C3 laceForO ld······
00000040 6B 65 79 01 C8 6F 6C 64  56 61 6C 75 65 E1 5A C8 key··old Value·Z·
00000050 6E 65 77 56 61 6C 75 65  E1 5A                   newValue ·Z      
```

receives:

```yaml
00000000 08 00 00 00 B9 05 72 65  70 6C 79 B0             ······re ply·    
```

### Key Set
example of checking the size of a keyset

sends:

```yaml
00000000 23 00 00 40 B9 03 63 73  70 EF 2F 2F 74 65 73 74 #··@··cs p·//test
00000010 3F 76 69 65 77 3D 4D 41  50 B9 03 74 69 64 A7 88 ?view=MA P··tid··
00000020 F4 47 AF 4D 01 00 00 0D  00 00 00 B9 06 6B 65 79 ·G·M···· ·····key
00000030 53 65 74 82 00 00 00 00                          Set·····         
```

receives:

```yaml
00000000 35 00 00 00 B9 05 72 65  70 6C 79 B6 09 73 65 74 5·····re ply··set
00000010 2D 70 72 6F 78 79 82 1E  00 00 00 B9 03 63 73 70 -proxy·· ·····csp
00000020 F2 2F 2F 74 65 73 74 3F  76 69 65 77 3D 6B 65 79 ·//test? view=key
00000030 53 65 74 B9 03 63 69 64  01                      Set··cid ·       
```

sends:

```yaml
00000000 14 00 00 40 B9 03 63 69  64 01 B9 03 74 69 64 A7 ···@··ci d···tid·
00000010 8A F4 47 AF 4D 01 00 00  0B 00 00 00 B9 04 73 69 ··G·M··· ······si
00000020 7A 65 82 00 00 00 00                             ze·····          
```

receives:

```yaml
00000000 07 00 00 00 C5 72 65 70  6C 79 05                ·····rep ly·     
```

### Put All
sends:

```yaml
00000000 23 00 00 40 B9 03 63 73  70 EF 2F 2F 74 65 73 74 #··@··cs p·//test
00000010 3F 76 69 65 77 3D 4D 41  50 B9 03 74 69 64 A7 4B ?view=MA P··tid·K
00000020 FD 47 AF 4D 01 00 00 0F  00 00 00 B9 08 65 6E 74 ·G·M···· ·····ent
00000030 72 79 53 65 74 82 00 00  00 00                   rySet··· ··      
```

receives:

```yaml
00000000 37 00 00 00 B9 05 72 65  70 6C 79 B6 09 73 65 74 7·····re ply··set
00000010 2D 70 72 6F 78 79 82 20  00 00 00 B9 03 63 73 70 -proxy·  ·····csp
00000020 F4 2F 2F 74 65 73 74 3F  76 69 65 77 3D 65 6E 74 ·//test? view=ent
00000030 72 79 53 65 74 B9 03 63  69 64 01                rySet··c id·     
```

sends:

```yaml
00000000 14 00 00 40 B9 03 63 69  64 01 B9 03 74 69 64 A7 ···@··ci d···tid·
00000010 4D FD 47 AF 4D 01 00 00  17 00 00 00 B9 10 6E 75 M·G·M··· ······nu
00000020 6D 62 65 72 4F 66 53 65  67 6D 65 6E 74 73 82 00 mberOfSe gments··
00000030 00 00 00                                         ···              
```

receives:

```yaml
00000000 07 00 00 00 C5 72 65 70  6C 79 01                ·····rep ly·     
```

sends:

```yaml
00000000 14 00 00 40 B9 03 63 69  64 01 B9 03 74 69 64 A7 ···@··ci d···tid·
00000010 4E FD 47 AF 4D 01 00 00  0B 00 00 00 B9 08 69 74 N·G·M··· ······it
00000020 65 72 61 74 6F 72 01                             erator·          
```

receives:

```yaml
00000000 6B 00 00 00 B9 05 72 65  70 6C 79 82 5F 00 00 00 k·····re ply·_···
00000010 82 0E 00 00 00 C3 6B 65  79 E1 34 C5 76 61 6C 75 ······ke y·4·valu
00000020 65 E1 44 82 0E 00 00 00  C3 6B 65 79 E1 35 C5 76 e·D····· ·key·5·v
00000030 61 6C 75 65 E1 45 82 0E  00 00 00 C3 6B 65 79 E1 alue·E·· ····key·
00000040 32 C5 76 61 6C 75 65 E1  42 82 0E 00 00 00 C3 6B 2·value· B······k
00000050 65 79 E1 33 C5 76 61 6C  75 65 E1 43 82 0E 00 00 ey·3·val ue·C····
00000060 00 C3 6B 65 79 E1 31 C5  76 61 6C 75 65 E1 41    ··key·1· value·A 
```

sends:

```yaml
00000000 23 00 00 40 B9 03 63 73  70 EF 2F 2F 74 65 73 74 #··@··cs p·//test
00000010 3F 76 69 65 77 3D 4D 41  50 B9 03 74 69 64 A7 4B ?view=MA P··tid·K
00000020 FD 47 AF 4D 01 00 00 67  00 00 00 B9 06 70 75 74 ·G·M···g ·····put
00000030 41 6C 6C 82 5A 00 00 00  82 0D 00 00 00 C3 6B 65 All·Z··· ······ke
00000040 79 05 C5 76 61 6C 75 65  E1 45 82 0D 00 00 00 C3 y··value ·E······
00000050 6B 65 79 01 C5 76 61 6C  75 65 E1 41 82 0D 00 00 key··val ue·A····
00000060 00 C3 6B 65 79 02 C5 76  61 6C 75 65 E1 42 82 0D ··key··v alue·B··
00000070 00 00 00 C3 6B 65 79 03  C5 76 61 6C 75 65 E1 43 ····key· ·value·C
00000080 82 0D 00 00 00 C3 6B 65  79 04 C5 76 61 6C 75 65 ······ke y··value
00000090 E1 44                                            ·D               
```

receives:

```yaml
00000000 0C 00 00 00 B9 05 72 65  70 6C 79 82 00 00 00 00 ······re ply·····
```

### Is Empty
example of isEmpty() returning true, not it uses the size() method

sends:

```yaml
00000000 23 00 00 40 B9 03 63 73  70 EF 2F 2F 74 65 73 74 #··@··cs p·//test
00000010 3F 76 69 65 77 3D 4D 41  50 B9 03 74 69 64 A7 DE ?view=MA P··tid··
00000020 0D 48 AF 4D 01 00 00 0B  00 00 00 B9 04 73 69 7A ·H·M···· ·····siz
00000030 65 82 00 00 00 00                                e·····           
```

receives:

```yaml
00000000 08 00 00 00 B9 05 72 65  70 6C 79 00             ······re ply·    
```

### Remove
sends:

```yaml
00000000 15 00 00 40 B9 03 63 73  70 EF 2F 2F 74 65 73 74 ···@··cs p·//test
00000010 3F 76 69 65 77 3D 4D 41  50 09 00 00 00 B9 06 72 ?view=MA P······r
00000020 65 6D 6F 76 65 05                                emove·           
```
### Values
example of getting the values and then calling size()

sends:

```yaml
00000000 23 00 00 40 B9 03 63 73  70 EF 2F 2F 74 65 73 74 #··@··cs p·//test
00000010 3F 76 69 65 77 3D 4D 41  50 B9 03 74 69 64 A7 31 ?view=MA P··tid·1
00000020 27 48 AF 4D 01 00 00 0D  00 00 00 B9 06 76 61 6C 'H·M···· ·····val
00000030 75 65 73 82 00 00 00 00                          ues·····         
```

receives:

```yaml
00000000 35 00 00 00 B9 05 72 65  70 6C 79 B6 09 73 65 74 5·····re ply··set
00000010 2D 70 72 6F 78 79 82 1E  00 00 00 B9 03 63 73 70 -proxy·· ·····csp
00000020 F2 2F 2F 74 65 73 74 3F  76 69 65 77 3D 76 61 6C ·//test? view=val
00000030 75 65 73 B9 03 63 69 64  01                      ues··cid ·       
```

sends:

```yaml
00000000 14 00 00 40 B9 03 63 69  64 01 B9 03 74 69 64 A7 ···@··ci d···tid·
00000010 33 27 48 AF 4D 01 00 00  0B 00 00 00 B9 04 73 69 3'H·M··· ······si
00000020 7A 65 82 00 00 00 00                             ze·····          
```

receives:

```yaml
00000000 07 00 00 00 C5 72 65 70  6C 79 05                ·····rep ly·     
```
