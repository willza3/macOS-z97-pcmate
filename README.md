# Mojave Clover Config Files for MSI Z97 PC MATE Motherboard.

<p align="center">
 <img src="https://preview.ibb.co/jmdrtp/Screenshot-2018-10-12-at-02-11-21.png"/>
</p>

Tested with macOS Mojave (10.14.0) but should work just fine with High Sierra (10.13.x)

## System Specifications
- **Motherboard:** MSI Z97 PC MATE
  * Networking: RealtekRTL8111
  * Audio Codec: Realtek ALC887
  
- **CPU:** Intel i5-4690K @ 3.5GHz

- **GPU:** ASUS STRIX AMD Radeon R9 390
  > Disable the **connectors kext patch** if you're having issues with graphics. The connectors are patched for ASUS STRIX cards and may not work properly with other brands.

## Not Working

- Stability issues when using DisplayPort

## Fix Blurry Font Rendering (Mojave)
macOS Mojave no longer supports subpixel antialiasing, making text on displays that are non "retina" look blurry. Enter in terminal to fix.

`defaults write -g CGFontRenderingFontSmoothingDisabled -bool NO`



## Credits

- [**Apple Inc.**](https://www.github.com/apple "Apple's GitHub Repo") for macOS
- [**acidanthera**](https://www.github.com/acidanthera "acidanthera's GitHub Repo") for AppleALC.kext and Lilu.kext
- [**corpnewt**](https://github.com/corpnewt "CorpNewt's GitHub Repo") for the audio tutorial
- [**netkas**](https://www.netkas.org "netkas's Blog") for FakeSMC.kext
- [**RehabMan**](https://www.github.com/rehabman "RehabMan's GitHub Repo") for RealtekRTL8111.kext
- [**Timo**](https://www.github.com/timocapa "Timo's GitHub Repo") for putting up with me
- [**vit9696**](https://www.github.com/vit9696 "vit9696's GitHub Repo") for Shiki.kext and WhateverGreen.kext

❤️
