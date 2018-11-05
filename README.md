# Dell Inspiron 5559

This repo is for the 15" Dell Inspiron 5559 i5-6200U. It should work for the 17" model.

# Supported Versions

`config.plist` is for Mojave.

# Working

* Microphone
* Bluetooth and Wifi - BCM94352Z https://www.newegg.com/Product/Product.aspx?Item=0XM-00BD-00004
* Display brightness
* IGPU (*NOTE: This computer has 64mb so no need to use any patching.*)
* Sleep
* Touchscreen (*NOTE: Completely independent of the OS. macOS does not natively support multi-touch*)
* Touchpad/Trackpad with all gestures
* Speakers (*Note: Use BoomAudio or eqMac to eliminate flat sound.*)
* USB 3 and 2

# Persistent Bugs & Errors

* CPU does not idle at 800MHz. It idles as low as 1.10GHz. Windows idles at 800MHz. Nothing appears to solve that.
* Upon reboot, WiFi or Bluetooth may be disabled. Shutdown completely to fix.
* Webcam. Intel RealSense F200 is a 3D camera and as a result does not work. It is classified as UVC, but requires drivers.
* Brightness buttons
* Pressing `FN` + `F9` results in a system hang. This is the search feature in Windows.
* Pressing `FN` + `F8` causes system lag. This is the project feature in Windows. 

# How to use

Clone this repo

# Post-Install

## S/L/E Kexts

Move the following kexts:
* Lilu
* WhateverGreen
* RealtekRTL8100
* CodecCommander
* AppleALC
* ACPIBatteryManager
* BrcmFirmwareRepo
* BrcmNonPatchRAM2
* BrcmPatchRAM2
* FakePCIID_Broadcom_WiFi
* FakePCIID

## L/E Kexts

Move the following kexts:
* AppleBacklightInjector

## Others

* This computer does not need any of the USB patches in config. USB Inject works but you need to patch the SSDT to properly show internal/external. It does not reach the port limit.
* Backlight SSDT needs to be generated before it will work.
* Optional: [System Prefs] > [Keyboard] > [Modifier Keys]. Change `Option` -> `Command` , `Command` -> `Option`

# TO DO

* Fix backlight buttons (ACPI proving difficult.)
* Could possilby grab a generic UVC replacement part from a slightly older, or variant model of this Dell.

# Notes

If your touchpad is not working, press `FN` + `PrtScr`. Pressing these buttons disables and enables it.
