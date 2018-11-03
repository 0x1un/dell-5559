# Dell Inspiron 5559

This repo is for the 15" Dell Inspiron 5559 i5-6200U. It should work for the 17" model.

# Supported Versions

`config.plist` is for Mojave.

# What works (and what doesn't)

* Microphone (webcam/mic combo, but no webcam)
* Bluetooth and Wifi - BCM94352Z https://www.newegg.com/Product/Product.aspx?Item=0XM-00BD-00004
* Display brightness (buttons do not)
* IGPU *NOTE: This computer has 64mb so no need to use any patching.*
* Sleep
* Touchscreen *NOTE: Completely independent of the OS. macOS does not natively support multi-touch*
* Touchpad/Trackpad with all gestures
* Speakers *Note: Use BoomAudio or eqMac to eliminate flat sound.*
* USB 3 and 2

# Persistent Bugs

* CPU does not idle at 800MHz. It idles as low as 1.10GHz. Windows idles at 800MHz. Nothing appears to solve that.
* Upon reboot, WiFi or Bluetooth will be disabled. Shutdown completely to fix.

# How to use

Clone this repo

# Post-Install

* This computer does not need any of the USB patches in config. USB Inject works but you need to patch the SSDT to properly show internal/external. It does not reach the port limit.
* Backlight SSDT needs to be generated before it will work.
* Once installed, move `Lilu`, `WhateverGreen`, and `RealtekRTL8100` kexts to S/L/E.
* Install `CodecCommander` to S/L/E
* Install `AppleALC.kext` to S/L/E
* Install `AppleBacklightInjector` to L/E
* Install `ACPIBatteryManager` to S/L/E
* Install `BrcmFirmwareRepo.kext`, `BrcmNonPatchRAM2.kext`, `BrcmPatchRAM2.kext`, to S/L/E
* Install `FakePCIID_Broadcom_WiFi.kext` and `FakePCIID.kext` to S/L/E
* This leave only esstential kexts in Clover for Recovery
* [System Prefs] > [Keyboard] > [Modifier Keys]. Change `Option` -> `Command` , `Command` -> `Option`

# TO DO

* Fix backlight buttons (ACPI proving difficult.)
* Webcam is Intel F200 UVC and appears active but displays no picture. `librealsense` does not detect it at all. Could possilby grab a generic UVC replacement part from a slightly older, or variant model of this Dell.

# Notes

I have had this laptop running smoothly since Mojave released.
