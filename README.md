# Dell Inspiron 5559

This repo is for the 15" Dell Inspiron 5559 i5-6200U. It should work for the 17" model.

# Supported Versions

`config.plist` has a seperate version for Sierra/High Sierra and Mojave.

# What works (and what doesn't)

* Microphone (webcam/mic commbo, but no webcam)
* Bluetooth (Intel card still present, so no wifi)
* Display brightness
* IGPU *NOTE: This computer has 64mb so no need to use kext patch*
* Sleep
* Touchscreen (Completely independent of the OS. macOS does not natively support multi-touch)
* Touchpad/Trackpad with all gestures
* Speakers *Note: Install VoodooHDA into Clover to prevent output reset on reboot*
* USB 3 and 2

# Persistent Bugs

* None at the moment


# How to use

Clone this repo or visit the releases tab.

Post-install this computer does not need USB inject all or any of the USB patches in config. You can remove them.

# TO DO

* Fix backlight buttons
* Webcam is Intel F200 UVC and appears active but displays no picture. AnyiSight kext does not correct this. Could be solved using USB patching instead of InjectAll. `librealsense` does not detect it at all.
