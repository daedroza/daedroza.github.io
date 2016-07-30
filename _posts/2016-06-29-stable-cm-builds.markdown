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
At level with CM
*From kernel_apq8064
f8198a7 fusion3 : update dogo, yuga, odin defconfig
dd31003 cleanups, align with upstream, fix merge errors
b0abf14 fs: fix mismerges
ea13a8f49 USB: core: Add USB_DEVICE_ERROR uevent for enumeration timeout
46557d4 USB: gadget: android: Fix checkpatch related errors
be75415 gadget: composite: Fix crash seen when SS descriptor is not available
40ee3fa usb: gadget: Set size only after validating pointer is valid
6b3ad71 usb: gadget: Validate the port number in acm_bind_config
f72d25a USB: gadget: android: Integrate f_midi USB MIDI gadget driver
7358ac9 USB: gadget: f_audio_source: Rename symbols to avoid conflicts with f_midi
{% endhighlight %}

Update #1 : 531f3f1 causes boot-loop at the moment. Reverted at the moment.

Update #2 : As of July 08, all branches expect kernel_apq8064 is even with CM's branches. Kernel is ahead ;-)

Update #3 : Switch to new msm8960 audio HAL.

Update #4 : Fixed alarm issue when system is suspended.

Update #5 : Added KSM, removed staging: zram and zmalloc. zram/zsmalloc has caused endless troubles. 

Update #6 : Added zram, zsmalloc, ksm, fixed denials.

Download link for fusion3 devices : [G-drive](https://drive.google.com/open?id=0B9yrk5QZnasiV1BaY1libUdBbWc)

Please use list-view and download for your proper device!

Happy Flashing!
