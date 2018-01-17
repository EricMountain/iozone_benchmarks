# IOZone benchmarks on ODroid HC1

All benchmarks run against a 64Gb SSD that had been previously been used
and not trimmed before starting these benchamrks.

* Self built kernel from ODroid GitHub with debug symbols (don't you just hate it when building with debug symbols makes a fully reproducible sudden death bug disappear?)
* iozone built from AUR.
* Stderr files are omitted as they were empty.
* `.report` files are "Excel compatible file(s) that contains the results".
* `.graph` files are plain text equivalents.

## Commands

## USB2

```
iozone -a -b ~/iozone.usb.ssd.report -R > ~/iozone.usb.ssd.graphs 2> ~/iozone.usb.ssd.stderr
```

## SATA

```
iozone -a -b ~/iozone.sata.ssd.report -R > ~/iozone.sata.ssd.graphs 2> ~/iozone.sata.ssd.stderr
```

## Machine data

```
[eric@crucible ~]$ uname -a
Linux crucible 4.14.0-rc8-1 #2 SMP PREEMPT Sat Nov 25 20:57:53 CET 2017 armv7l GNU/Linux

[eric@crucible ~]$ lscpu
Architecture:        armv7l
Byte Order:          Little Endian
CPU(s):              8
On-line CPU(s) list: 0-7
Thread(s) per core:  1
Core(s) per socket:  4
Socket(s):           2
Model:               3
Model name:          ARMv7 Processor rev 3 (v7l)
CPU max MHz:         2000.0000
CPU min MHz:         200.0000
BogoMIPS:            84.00
Flags:               half thumb fastmult vfp edsp neon vfpv3 tls vfpv4 idiva idivt vfpd32 lpae

[eric@crucible ~]$ iozone -v
       'Iozone' Filesystem Benchmark Program

        Version $Revision: 3.471 $
        Compiled for 32 bit mode.
[…]
```
