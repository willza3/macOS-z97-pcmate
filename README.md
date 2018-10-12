# Mojave Clover Config Files for MSI Z97 PC MATE Motherboard.

<p align="center">
 <img src="https://ibin.co/4In2flcxe4x8.jpg"/>
</p>

## System Specifications
Tested with macOS Mojave (10.14.x) but should work just fine with High Sierra (10.13.x)

- **Motherboard:** MSI Z97 PC MATE
  * Networking: RealtekRTL8111
  * Audio Codec: Realtek ALC887
  
- **CPU:** Intel i5-4690K @ 3.5GHz

- **GPU:** ASUS STRIX AMD Radeon R9 390
  > Disable the **connectors kext patch** if you're having issues with graphics. The connectors are patched for ASUS STRIX cards and may not work properly with other brands.

## Known Issues

- Using DisplayPort can cause issues with video output, such as no signal.
  > Workaround: Use an alternative connection, such as HDMI.
 
- "Sleeping" for a long time can cause system instability upon wake.
  > Workaround: Increase the length of time required until entering sleep in System Preferences.

## Fix Blurry Font Rendering (10.14+)

Starting with Mojave, subpixel anti-aliasing is no longer supported on macOS, causing text on displays that are "non-retina" to look blurry. Enter this command in a terminal window to fix.

`defaults write -g CGFontRenderingFontSmoothingDisabled -bool NO`



## Credits

- [**Apple Inc.**](https://www.github.com/apple "Apple's GitHub Repo") for macOS
- [**acidanthera**](https://www.github.com/acidanthera "acidanthera's GitHub Repo") for AppleALC.kext and Lilu.kext
- [**carpentryplus25**](https://www.tonymacx86.com/threads/guide-how-to-patch-amd-framebuffers-for-high-sierra-using-clover.235409/ "carpentryplus25's Patching Tutorial") for the AMD framebuffer patching tutorial
- [**corpnewt**](https://github.com/corpnewt "CorpNewt's GitHub Repo") for the audio tutorial
- [**netkas**](https://www.netkas.org "netkas's Blog") for FakeSMC.kext
- [**RehabMan**](https://www.github.com/rehabman "RehabMan's GitHub Repo") for RealtekRTL8111.kext
- [**Timo**](https://www.github.com/timocapa "Timo's GitHub Repo") for putting up with me
- [**vit9696**](https://www.github.com/vit9696 "vit9696's GitHub Repo") for Shiki.kext and WhateverGreen.kext

❤️
