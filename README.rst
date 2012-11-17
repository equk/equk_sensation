equk_sensation
==============

This section has a few scripts I have written for tweaking/hacking the Google Android OS

Most of it is aimed specifically at the HTC Sensation/XE

.. code-block:: bash

	Device: HTC Sensation

	Chipset: Qualcomm MSM8260 Snapdragon
	CPU: Dual-core 1.566 GHz Scorpion
	GPU: Adreno 220
	Display: 4.3 Inch S-LCD Capacitive
	Resolution: 540 x 960 pixels
	Protection: Corning Gorilla Glass
	Camera: 8 MP, 3264x2448 pixels
	        autofocus, dual-LED flash

	OS: Google Android Jellybean v4.1.2

	Firmware: 3.33
	Features: S-OFF, Unlocked, Rooted, SuperCID

Current ROM
-----------

* OS: Jellybean v4.1.2
* Kernel: Linux 3.0.51
* Patched 4.2 Camera
* 4.2 Swype Style Keyboard
* Recovery: CWM 5.0.2.0
* PDroid 1.32
* Paranoid Android
* Custom Kernel Init Scripts

*Kernel Source:* https://github.com/bruce2728/android_kernel_htc_pyramid

*Paranoid Android:* http://paranoid-rom.com/

**Tweaks**

* Dalvik Tweaks
* Kernel Mem Tweaks
* DNS forced to OpenDNS
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

.. code-block:: bash

	cat /data/equk_kernel.log
	Setting Kernel Preferences - 11-07-2012 12:19:01
	setting fast charge to 0
	setting sweep2wake to 0
	setting governor to to ondemand
	setting scheduler to to noop
	Setting drop caches

memory before and after linux kernel drop caches tweak

.. code-block:: bash

	n		 total         used         free       shared      buffers
	Mem:        595664       532216        63448            0        20100
	-/+ buffers:             512116        83548
	Swap:            0            0            0
	n		 total         used         free       shared      buffers
	Mem:        595664       320424       275240            0          212
	-/+ buffers:             320212       275452
	Swap:            0            0            0

**90equk_zipalign**

zipalign everything installed to /data/app/ (as everything in /system/app/ should already be aligned)


.. image:: https://github.com/equk/equk_sensation/raw/master/screenshot.png
   :align: center
   :alt: android_screenshot
