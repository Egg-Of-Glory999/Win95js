---
layout: page
title: PCjs Machine Command-Line Utility
permalink: /tools/pc/
redirect_from: /machines/pcx86/modules/bin/
---

This directory contains the PCjs machine command-line utility [PC.js](pc.js), which allows you to start a "headless" machine with all TTY (eg, INT 0x10) output redirected to your console.

Load a JSON machine file, such as [ibm5150.json5](ibm5150.json5) or [compaq386.json5](compaq386.json5), with the utility's `load` command, either interactively or with the `--load` command-line argument.

For example, this command:

	pc.js --load=ibm5150

or, if your operating system doesn't automatically associate `.js` files with [Node](https://nodejs.org/en), this command:

	node pc.js --load=ibm5150

should produce the following output:

    PCx86 v2.00
    Copyright © 2012-2023 Jeff Parsons <Jeff@pcjs.org>
    License: MIT <https://www.pcjs.org/LICENSE.txt>
    BusX86: 32Kb ROM at 0xF6000
    BusX86: 8Kb ROM at 0xFE000
    Machine loaded: ibm5150
    Press ctrl-a to enter debugger, ctrl-c to terminate debugger
    FDC: Mounted "PC DOS 2.00 (Disk 1)" (format PC180K) in drive A
    BusX86: 576Kb RAM at 0x0
    BusX86: 4Kb VIDEO at 0xB0000
    Type ? for help with PCx86 Debugger commands
    AX=0000 BX=0000 CX=0000 DX=0000 SP=0000 BP=0000 SI=0000 DI=0000 
    SS=0000 DS=0000 ES=0000 PS=F002 V0 D0 I0 T0 S0 Z0 A0 P0 C0 
    &FFFF:0000 EA5BE000F0       JMP      &F000:E05B (romBIOS+0x005B)
    running

After the machine finishes booting (about 10 seconds), you should see the following output:

    Current date is Tue  1-01-1980
    Enter new date: 

You can begin interacting with the machine OR you can press CTRL-A to enter the PCjs debugger.  For example, if you'd like to dump the machine's video buffer, press CTRL-A and type `D B000:0`:

    Enter new date: stopped (326282712 cycles, 68534 ms, 4760888 hz)
    AX=0091 BX=0165 CX=0586 DX=007F SP=0BAA BP=0535 SI=0140 DI=01AA 
    SS=00DB DS=0070 ES=00DB PS=F246 V0 D0 I1 T0 S0 Z1 A0 P1 C0 
    &0070:0125 CB               RETF    
    >> D B000:0  
    &B000:0000  43 07 75 07 72 07 72 07-65 07 6E 07 74 07 20 07  C.u.r.r.e.n.t. .
    &B000:0010  64 07 61 07 74 07 65 07-20 07 69 07 73 07 20 07  d.a.t.e. .i.s. .
    &B000:0020  54 07 75 07 65 07 20 07-20 07 31 07 2D 07 30 07  T.u.e. . .1.-.0.
    &B000:0030  31 07 2D 07 31 07 39 07-38 07 30 07 20 07 20 07  1.-.1.9.8.0. . .
    &B000:0040  20 07 20 07 20 07 20 07-20 07 20 07 20 07 20 07   . . . . . . . .
    &B000:0050  20 07 20 07 20 07 20 07-20 07 20 07 20 07 20 07   . . . . . . . .
    &B000:0060  20 07 20 07 20 07 20 07-20 07 20 07 20 07 20 07   . . . . . . . .
    &B000:0070  20 07 20 07 20 07 20 07-20 07 20 07 20 07 20 07   . . . . . . . .
    >> 

To destroy the machine, type `quit` (or press CTRL-C) at the debugger prompt.

[PC.js](https://github.com/jeffpar/pcjs/tree/master/tools/pc) is more general-purpose than its predecessor, [pcx86.js](https://github.com/jeffpar/pcjs/tree/2ac6e5e62196212bede02f360634f04a9c358ed9/machines/pcx86/bin), and can theoretically load any other machine type listed in [machines.json](/machines/machines.json), but it has only been tested with `pcx86` and `pdp11` machines so far.

This utility is very much a "work in progress" and is intended for development work and testing only.  Also, since it is "headless", you will not see any output from the machine when running any software that writes directly to video memory.

### Support for XML Machine Files

Limited support for XML-based machines now exists; eg:

    pc.js --load=/machines/pcx86/ibm/5170/ega/1024kb/rev3/debugger/machine.xml

loads and runs the same [machine.xml](/machines/pcx86/ibm/5170/ega/1024kb/rev3/debugger/machine.xml) that also exists on the PCjs website.

And here's another example using a `pdp11` [machine.xml](/machines/dec/pdp11/1170/panel/debugger/machine.xml):

    pc.js --load=/machines/dec/pdp11/1170/panel/debugger/machine.xml

### Dynamic Access to Local Files from MS-DOS

If you run [pc.js](pc.js) with the name of DOS executable in your current directory; eg:

    pc.js pkunzip.exe

it will automatically build a 10Mb MS-DOS hard disk image in the `/tools/pc` folder with all the files/folders in your current directory and then load the [compaq386](compaq386.json5) machine with that disk image mounted as drive C.

One of the pre-requisites of this feature is having a copy of the [pcjs-diskettes](https://github.com/jeffpar/pcjs-diskettes) repository in the `/disks/diskettes` folder of your PCjs repository:

    cd pcjs
    mkdir disks
    cd disks
    git clone https://github.com/jeffpar/pcjs-diskettes.git diskettes

because [pc.js](pc.js) uses system files from MS-DOS diskettes (eg, [MSDOS320-DISK1](https://github.com/jeffpar/pcjs-diskettes/blob/master/pcx86/sys/dos/microsoft/3.20/MSDOS320-DISK1.json)) to build a bootable hard disk image.

### Historical Notes

One early use of this utility was running a set of [80386 CPU Tests](https://github.com/jeffpar/pcjs/blob/master/software/pcx86/test/cpu/80386/test386.asm) as a custom ROM image inside an [80386 Test Machine](https://github.com/jeffpar/pcjs/blob/master/tools/pc/test386.json5), and then comparing the results to [output](/software/pcx86/test/cpu/80386/test386.txt) from real hardware.

The test program ([test386.asm](/software/pcx86/test/cpu/80386/test386.asm)) was carefully designed to be built as a binary (`test386.com`) that could either be run as a DOS program *or* loaded as a ROM image.  See [PCx86 CPU Tests](/software/pcx86/test/cpu/) for more information.