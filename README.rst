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
* Kernel: Linux 3.0.50
* Patched 4.2 Camera
* 4.2 Swype Style Keyboard
* Recovery: CWM 5.0.2.0
* PDroid 1.32
* Paranoid Android

Custom Tweaks
-------------

* RIL Tweaks for better signal
* Dalvik Tweaks for performance
* Memory Tweaks via linux kernel
* DNS forced to OpenDNS
* Custom hosts file for AdBlocking
* Custom SSH Tunnel scripts
* VPN Tun Adapter
* Youtube custom tablet mode
* Beats Audio

Startup Scripts
---------------

.. code-block:: bash

	echo 3 > /proc/sys/vm/drop_caches

memory before and after linux kernel mem tweak

.. code-block:: bash

	n			 total         used         free       shared      buffers
	Mem:        595664       532216        63448            0        20100
	-/+ buffers:             512116        83548
	Swap:            0            0            0
	n			 total         used         free       shared      buffers
	Mem:        595664       320424       275240            0          212
	-/+ buffers:             320212       275452
	Swap:            0            0            0



.. image:: https://github.com/equk/equk_sensation/raw/master/screenshot.png
   :align: center
   :alt: android_screenshot
