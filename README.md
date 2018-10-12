# Dell Inspiron 5559

This repo is for the 15" Dell Inspiron 5559 i5-6200U. It should work for the 17" model.

# Supported Versions

`config.plist` has a seperate version for Sierra/High Sierra and Mojave.

# What works (and what doesn't)

* Microphone (webcam/mic commbo, but no webcam)
* Bluetooth (Intel card still present, so no wifi)
* Display brightness (buttons do not)
* IGPU *NOTE: This computer has 64mb so no need to use kext patch*
* Sleep
* Touchscreen *NOTE: Completely independent of the OS. macOS does not natively support multi-touch*
* Touchpad/Trackpad with all gestures
* Speakers *Note: Install VoodooHDA into Clover to prevent output reset on reboot*
* USB 3 and 2

# Persistent Bugs

* CPU does not idle at 800MHz. It idles at 1.30GHz. Windows idles at 800MHz. Nothing appears to solve that.

# How to use

Clone this repo or visit the releases tab.

# Post-Install

* This computer does not need USB inject all or any of the USB patches in config. Do not inject or patch anything.
* This computer functions better with a generated SSDT for power management. Battery life is the same as Windows.
* Backlight SSDT needs to be generated before it will work.
* Install CodecCommander to S/L/E
* Install AppleBacklightInjector to L/E
* Install ACPIBatteryManager to S/L/E
* [System Prefs] > [Keyboard] > [Modifier Keys]. Change `Option` -> `Command` , `Command` -> `Option`

# TO DO

* Fix backlight buttons
* Webcam is Intel F200 UVC and appears active but displays no picture. `librealsense` does not detect it at all.
