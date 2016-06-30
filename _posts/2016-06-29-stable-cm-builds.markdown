---
layout: post
title: Stable CM-builds
description: "Stable cm-builds for the community!"
mathjax: true
date:   2016-06-29 15:30:28 +0530
typefix:
     indent: true
image:
     feature: "https://upload.wikimedia.org/wikipedia/en/thumb/1/10/CyanogenMod_logo.svg/1524px-CyanogenMod_logo.svg.png"
---

Hello, this is a 14-days/monthly buildbot for fusion3 devices. Remember, they are made from last-known stable
configuration to me. Additionally, I have done some cherry-picks, including rotation sensor fix.
I assume that you have already read all the stuff from the xda-thread corresponding to this and only then head
over to downloads!
{% highlight bash %}
From fusion3-common
3dd2c32 fusion3-common: Use MONOTONIC for rotation sensor timestamp
531f3f1 fusion3-common: Update custombootimg for renamed toybox_init
c5be746 init: remove no_sleep from mpdecision

From kernel_apq8064
6392ba2 cpu: Fix generic idle thread allocation
b84c9d8 arm: Use generic idle thread allocation
788cd32 smp: Add task_struct argument to __cpu_up()
de18ee1 CPU hotplug: Provide lockless versions of callback registration functions
22d0ae9 power: remove earlysuspend
{% endhighlight %}

Update : 531f3f1 Doesn't work.... That's probably everyone is using TWRP for flashing and not cm's recovery...
so I have reverted at the moment... new builds with fix will be up soon :-)

Download link for fusion3 devices : [G-drive](https://drive.google.com/open?id=0B9yrk5QZnasiV1BaY1libUdBbWc)

Please use list-view and download for your proper device!

Happy Flashing!
