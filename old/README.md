This folder contains a lot of older scripts written for jellybean / kernel 3.0

Most of these are integrated into KitKat and so are not really used anymore

**Tweaks**

* Dalvik Tweaks
* Kernel Mem Tweaks
* Custom hosts file for AdBlocking
* Custom SSH Tunnel scripts (redsocks)

Startup Scripts
---------------

**85equk_kernel**

* set kernel based settings on startup (usb fast charge, sweep2wake, cpu governor, I/O scheduler)
* install kernel modules on startup if flagged (tun.ko)
* start zram if required
* enable kernel drop caches

example log:

    cat /data/equk_kernel.log
    Setting Kernel Preferences - 11-07-2012 12:19:01
    setting fast charge to 0
    setting sweep2wake to 0
    setting governor to to ondemand
    setting scheduler to to noop
    Setting drop caches

memory before and after linux kernel drop caches tweak

    n        total         used         free       shared      buffers
    Mem:        595664       532216        63448            0        20100
    -/+ buffers:             512116        83548
    Swap:            0            0            0
    n        total         used         free       shared      buffers
    Mem:        595664       320424       275240            0          212
    -/+ buffers:             320212       275452
    Swap:            0            0            0

**90equk_zipalign**

zipalign everything installed to /data/app/ (as everything in /system/app/ should already be aligned)
