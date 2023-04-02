---
layout: page
title: "PC-SIG Library Disk #307"
permalink: /software/pcx86/sw/misc/pcsig/0001-0999/DISK0307/
machines:
  - id: ibm5160
    type: pcx86
    config: /machines/pcx86/ibm/5160/cga/256kb/machine.xml
    diskettes: /machines/pcx86/diskettes.json,/disks/pcsigdisks/pcx86/diskettes.json
    autoGen: true
    autoMount:
      B: "PC-SIG Library Disk 0307"
    autoType: $date\r$time\rB:\rDIR\r
---

{% include machine.html id="ibm5160" %}

## Information about "ASSEMBLY UTILITIES NO 1"

    The programs on this disk are utilities for hackers or experienced
    programmers.  They do many different things and most are aimed at
    system operations and DOS commands.  Routines include on-screen
    calculator, and a disk drive alignment program.
    
    System Requirements: Optional 8087 co-processor
    
    How to Start: To read DOC or TXT files, enter TYPE filename.ext and
    press <ENTER>.  To run an EXE or COM program, just type its name and
    press <ENTER>.  For instructions on running BASIC programs, please
    refer to the GETTING STARTED section in this catalog.
    
    File Descriptions:
    
    87ERROR  COM  Handles error calls from optional 8087 math co-processor
    87ERROR  ASM  Assembly source for 87ERROR
    87ERROR  DOC  Documentation for 87ERROR
    ALIGN    BAS  Head alignment program
    87ERROR  OBJ  Part of 87ERROR
    AST-TEST COM  Memory test program
    ASCII    COM  Displays ASCII table on screen
    ANSIKEYS DOC  Documentation for ANSI&2K
    ANSI&2K  SYS  Expands function key buffer by 2k
    SYSTAT   COM  Displays name and comments of each disk drive in system
    SYSTAT   DOC  Documentation for SYSTAT
    TEE      COM  Allows you to see what is being piped in piping commands
    UNDOBKUP BAS  Same as UNDO
    UNDO     BAS  Allows fixed disk users to read backup diskettes
    TESTDRV  BAS  Performs read/write test on drives
    TEE      DOC  Documentation for TEE
    CALC     EXE  On screen calculator
    BDNCHM   TXT  A fast and dirty function accuracy test
    CLEARRO  COM  Clears read only attribute from files
    CIPHER   BAS  A simple encoding and decoding security system
    CORELOOK COM  Takes snapshot of memory core
    CLEARRO  DOC  Docs for CLEARRO
    DEBUG    TXT  A small tutorial about the DEBUG command in DOS
    CURSOR   DOC  Documentation for CURSOR
    CURSOR   COM  Sets maximum size of cursor
    CPMDOSXR DOC  Displays equivelent commands in DOS and CP/M
    DEFRAG   BAS  Unifies a file that is fragmented by repeated use
    DEFRAG   DOC  Documentation for DEFRAG
    DOS-BUG  4E   Reports on bug in DOS 2.1 function calls
    ENVINUSE COM  Sizes environment buffer
    DOS2A    TXT  Information about DOS 2.0 interrupts
    MEMORY   DOC  Docs to explain MEMORY
    MEMORY   COM  Allows dynamic memory switch change
    LOOKMEM  COM  Another memory look program
    KEYS          Optional key assignment list
    ENVXPAND SYS  Expands environment buffer by 1k
    ENVIRO   PAT  Patches COMMAND.COM for larger environement area
    ENVXPAND DOC  Documentation for ENVXPAND
    ENVIRON  DOC  Explains some of the SET command options
    SETVAR   DOC  Documentation for SETVAR
    SETVAR   COM  Allows variables and variations to the set command
    SETRO    DOC  Documentation for SETRO
    SETRO    COM  Sets read only parameter to on
    SETKEY   EXE  Allows user redefinition of keyboard
    SETKEY   DOC  Documentation for SETKEY
    REBOOT   EXE  Software system reboot
    REBOOT   DOC  Brief apologetic note explaining lack of documentation
    QUIKUPQD COM  Part of QUIKUP
    QUIKUP   DOC  Documentation for QUIKUP
    QUIKUP   COM  Faster bootup by use of software memory switches
    PARINT   COM  Parity intercept
    NULLKEYS      Optional key assignment list
    MORERAM  DOC  Docs for MORERAM
    MORERAM  COM  Allows PC to use more RAM then switch sets suggest
    MORERAM  ASM  Assembler source for MORERAM

### Directory of PC-SIG Library Disk 0307

     Volume in drive A has no label
     Directory of A:\

    ANSI&2K  SYS      4096   1-13-84   7:13a
    ANSIKEYS DOC      6039   1-13-84   8:34a
    AST-TEST COM      4608   3-02-84   6:46a
    BDNCHM   TXT       896   6-07-84   5:26p
    CLEARRO  COM      1787   6-18-84   1:26a
    SETVAR   COM       512   1-06-85   9:20a
    SETVAR   DOC      1280   1-06-85   9:21a
    CIPHER   BAS       640  10-26-83   4:18p
    TEE      DOC       173   1-27-85  11:24a
    TEE      COM       281   9-07-83   8:26a
    87ERROR  ASM      1938   5-05-84   8:59p
    DOS2A    TXT      1536   3-07-84   6:38a
    ENVIRON  DOC      2560   3-07-84   6:37a
    DEBUG    TXT     34560  12-23-84  10:34a
    ALIGN    BAS      1024   7-25-83   8:29a
    KEYS              2560   1-13-84   7:17a
    87ERROR  COM       120   5-05-84   9:00p
    87ERROR  DOC      1601   5-05-84   8:49p
    MEMORY   COM      1532   6-23-83  10:33a
    MEMORY   DOC      2599   6-23-83  10:49a
    87ERROR  OBJ       226   5-05-84   9:00p
    CLEARRO  DOC      1536   6-18-84   1:10a
    MORERAM  ASM      7168   1-02-84   1:09a
    MORERAM  COM       512   1-02-84   1:07a
    MORERAM  DOC      3456   1-02-84   1:06a
    NULLKEYS          2560   1-13-84   7:16a
    REBOOT   DOC       179   3-08-83  12:04a
    REBOOT   EXE       640   8-29-82   1:05a
    CURSOR   COM       654   6-18-84   1:27a
    DOS-BUG  4E        426   5-03-84   5:53p
    SETKEY   DOC      2432   7-11-83   7:54a
    SETKEY   EXE     32256   7-13-83   6:48a
    CURSOR   DOC       768   6-18-84   1:09a
    SYSTAT   COM      1536   6-05-83   7:22a
    SYSTAT   DOC      1024   6-05-83   7:21a
    TESTDRV  BAS      2048   7-02-83  10:02a
    SETRO    COM      1771   6-18-84   1:23a
    UNDO     BAS      4608   2-21-84   6:56a
    UNDOBKUP BAS      2048   1-02-84   1:05a
    SETRO    DOC      1536   6-18-84   1:09a
    DEFRAG   BAS      5888   4-29-84   8:39p
    CORELOOK COM      5120   1-01-80   1:35a
    DEFRAG   DOC      5019   4-29-84   8:39p
    ENVIRO   PAT      1340   8-18-84  11:26a
    LOOKMEM  COM      1335   7-26-84   6:20p
    CPMDOSXR DOC      9472   9-12-83   3:29p
    ASCII    COM      6774   9-15-84   8:01p
    CALC     EXE     15698  12-23-84   5:15p
    ENVXPAND SYS      3200  12-28-84  11:14p
    ENVXPAND DOC      3328  12-28-84  11:14p
    ENVINUSE COM       512  12-28-84  11:14p
    PARINT   COM       512  12-28-84   6:17p
    QUIKUP   COM       192   7-10-83   1:28p
    QUIKUP   DOC      1675  10-13-84  12:00p
    QUIKUPQD COM       185   7-10-83   1:56p
    FILES307 TXT      3142   2-02-87   4:13p
           56 file(s)     201118 bytes
                           95232 bytes free