# OpenCore for HP Pavilion 15-cs2033TU (Hackintosh)

## Note Before using this pre-make OpenCore

1. Double-check the specification.
2. Please change the SMBIOS information by using GenSMBIOS [here](https://github.com/corpnewt/GenSMBIOS). Tutorial? Check [this one](https://dortania.github.io/OpenCore-Install-Guide/config-laptop.plist/coffee-lake.html#platforminfo) and focus on platforminfo.
3. Some components wouldn't work because I changed them like add an NVME SSD and replace the original Wi-Fi card with the Macbook's one.

## Specification:

- Brand: HP Pavilion 15.
- Model: 15-cs2033tu.
- CPU: Intel i5-8265U (Whiskey Lake) 1.6-3.9 GHz - Intel UHD 620 (fake to UHD 630 Mobile) - 2048MB.
- RAM: SAMSUNG 8GB x 2 (2400 MHz).
- HDD: 1TB WD.
- SSD: 256GB WD WDS500G2B0C-00PXH0.
- Wi-Fi: Replaced Intel Wireless-AC 9461 by BCM94360CS (Use [itlwm](https://github.com/OpenIntelWireless/itlwm) and [HeliPort](https://github.com/OpenIntelWireless/HeliPort) if you still don't have a better Wi-Fi card).
- LAN: Realtek RTL8168H/8111H kext.
- Touchpad: ELAN ETD074C (074C). ~~Turn off by pressing <kbd>prc sc</kbd>.~~
- Audio: Realtek ALC295 (layout-id=28) (Shutdown after dual-boot with Windows to reset audio state on macOS). Fix the external mic by [ALCPlugFix](https://github.com/black-dragon74/ALCPlugFix-Swift) (use Node ID=0x19 and install Homebrew before using ALCPlugFix).
- Battery: HT03XL size (Work perfectly, information show up).

## What doesn't work:

- ~~Hotkey adjusts the brightness.~~ (fixed via this [kext](https://github.com/acidanthera/BrightnessKeys))
- ~~Battery indicator.~~ (fixed via this [post](https://www.reddit.com/r/hackintosh/comments/n2nvf8/ecenabler_no_more_acpi_patches_for_battery_sorta/))
- ~~Need improvement for the touchpad.~~ (Updated new VoodooPS2.kext)
