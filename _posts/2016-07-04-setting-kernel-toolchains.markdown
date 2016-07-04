---
layout: post
title: Toolchain for kernel development
description: "Solving the riddle in POST #1(2016-06-29)"
mathjax: true
date:   2016-07-04 15:30:28 +0530
typefix:
     indent: true
image:
     feature: "https://www.quadranet.com/wp-content/uploads/2014/04/logo-linux-1-566x190.jpg"
---

A week and a half ago, I was cherry-picking some thermal commits for Airless kernel. To check whether the kernel had any compliation error, I went straight ahead to the kernel directory. I properly set up my toolchain paths and tried compiling using make -j16.

A error came where the toolchain wasn't able to recognize the flags while building kernel. I was skeptical since it was first time I ever encountered something like this after my switch to Mint 18. So I googled around, asked some communities. There was no answer to fix the issue. I tried a lot of searching and found a lot of different ways of setting the paths. I had failed that day and probably ended up setting this website!

Here is the error : 
{ % highlight bash %}
gcc: error: unrecognized argument in option ‘-mabi=aapcs-linux’
gcc: note: valid arguments to ‘-mabi=’ are: ms sysv
gcc: warning: ‘-mcpu=’ is deprecated; use ‘-mtune=’ or ‘-march=’ instead
gcc: error: unrecognized command line option ‘-mlittle-endian’
gcc: error: unrecognized command line option ‘-mapcs’
gcc: error: unrecognized command line option ‘-mno-sched-prolog’
gcc: error: unrecognized command line option ‘-mno-thumb-interwork’
gcc: error: unrecognized command line option ‘-munaligned-access’
gcc: error: unrecognized command line option ‘-marm’
gcc: error: unrecognized command line option ‘-mfpu=neon-vfpv4’
make[1]: *** [kernel/bounds.s] Error 1
make: *** [prepare0] Error 2
make: *** Waiting for unfinished jobs....
make: *** [scripts] Error 2
{ % endlight % }


However, I reverted all my commits and went back to square one. I restarted all my stuff I had been working on. Now, I use Google's method to setup the toolchain. You obviously need a nice toolchain that optimizes and compiles your ROM. I used version 5.3 from UBERTC. And the way google does it :
{ % highlight bash %}
export PATH=/path/to/tool/chain/bin:$bin
export CROSS_COMPILE=prefixoftoolchain-
export ARCH=arm or arch or for type of device you're building
{ % endlight % }


