---
layout: post
title: Stable CM-builds
description: "Cyanogenmod 13 for Z|ZR|ZL"
mathjax: true
date:   2016-06-29 15:30:28 +0530
typefix:
     indent: true
image:
     feature: "https://upload.wikimedia.org/wikipedia/en/thumb/1/10/CyanogenMod_logo.svg/1524px-CyanogenMod_logo.svg.png"
---

Hello, this is a 14-days/monthly buildbot for fusion3 devices. Remember, they are made from last-known stable
configuration to me. Additionally, I have done some cherry-picks, including rotation sensor fix.
I assume that you have already read all the stuff from the xda-thread([ZL](http://forum.xda-developers.com/xperia-zl/development/stable-cyanogenmod-t3407662)|[Z](http://forum.xda-developers.com/xperia-z/development/stable-cyanogenmod-t3407658)|[ZR](http://forum.xda-developers.com/xperia-zr/development/stable-cyanogenmod-t3407650)) corresponding to this and only then head
over to downloads!

{% highlight bash%}
*From fusion3-common
69e78e2 fusion3: Fix incall audio
f6a610b fusion3-common: Use MONOTONIC for rotation sensor timestamp
738117a fusion3-common: Update custombootimg for renamed toybox_init
37253dc init: switch to interactive cpu gov
*From kernel_apq8064
34650ee lockdep: Remove unnecessary 'hlock_next' variable
5268fbc lockdep: Consolidate bug messages into a single print_lockdep_off() function
6d98513 lockdep: Print out additional debugging advice when we hit lockdep BUGs
f0b46e9 lockdep: Print more info when MAX_LOCK_DEPTH is exceeded
f5bd7db lockdep: Rename print_unlock_inbalance_bug() to print_unlock_imbalance_bug()
8c68a4e kernel: Mark find_task_by_vpid with EXPORT_SYMBOL_GPL
531a7f8 printk: Complete the backport
{% endhighlight %}

Update #1 : 531f3f1 causes boot-loop at the moment. Reverted at the moment.

Update #2 : As of July 08, all branches expect kernel_apq8064 is even with CM's branches. Kernel is ahead ;-)

Update #3 : Switch to new msm8960 audio HAL.

Update #4 : Fixed alarm issue when system is suspended.

Download link for fusion3 devices : [G-drive](https://drive.google.com/open?id=0B9yrk5QZnasiV1BaY1libUdBbWc)

Please use list-view and download for your proper device!

Happy Flashing!
