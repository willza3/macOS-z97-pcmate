# High Sierra Clover Config Files for MSI Z97 PC MATE Motherboard.

## Introduction 

<p align="center">
 <img src="https://preview.ibb.co/d9uZj8/Screen_Shot_2018_07_15_at_09_56_04.png"/>
</p>

**Looking for Mojave?** [Config here](https://github.com/willza3/z97-pcmate-mojave/blob/master/README.md)
This is my personal Clover configuration file. I own **none** of the files provided, all rights go to their original owners.

## System Specifications
- **Motherboard:** MSI Z97 PC MATE
  * Networking: RealtekRTL8111
  * Audio Codec: Realtek ALC887
  
- **CPU:** Intel i5-4690K @ 3.5GHz

- **GPU:** AMD Radeon R9 390
  > The **AMDController8000.kext** will need to be patched for the R9 390 to work properly. A tutorial on this is provided            below.
  
This document is assuming you have the same hardware configuration as me, tested with macOS "High Sierra" 10.13.6 (Build 17G65)

## Not Working

- iGPU + GPU
  > Enabling the iGPU in BIOS settings breaks video output.

- ???

## Untested
- WiFi

- Bluetooth

- Camera

## Patches and Fixes

### Patching AMDController8000.kext to support R9 390

1. Follow steps 5-12 of [this tutorial.](https://www.tonymacx86.com/threads/guide-getting-r9-290-390-non-x-to-work-on-sierra-10-12-and-high-sierra-10-13.210574/) Ignore the first section telling you to change your BIOS settings

2. Mount your EFI Partition and import your config.plist into Clover Configurator

3. Select the devices tab and under "Fake ID", enter '0x067B01002' into the ATI text-box

4. Select the graphics tab and type "Radeon" into the "FB Name" text-box, **make sure that "Inject ATI" is ticked**

5. Save your new config.plist file and make sure it's placed in 'EFI -> CLOVER -> config.plist'

6. Make sure that the latest versions of the AppleALC, Lilu and WhateverGreen kexts are present in your clover configuration

7. Save your new configuration file and reboot into macOS

### Fixing USB 3.0

1. Mount your EFI Partition and import your config.plist into Clover Configurator

2. Select the ACPI tab and check "USB" under the "Drop OEM_DSM" checkbox

3. Save your new configuration file and reboot into macOS

### Fixing Broken Audio

[Follow this tutorial to fix audio](https://www.reddit.com/r/hackintosh/comments/4sil5p/audio_mechanic_old_patchfix_removal_applealc/)

### Fixing Incorrect CPU Identifier in About This Mac and System Information

1. Mount your EFI Partition and import your config.plist into Clover Configurator

2. Select the CPU tab and change type to 0x0306C0

3. Set Frequency MHz to your processor's frequency

4. Save your new configuration file and reboot into macOS

## Credits

- [**Apple Inc.**](https://www.github.com/apple "Apple's GitHub Repo") for macOS
- [**acidanthera**](https://www.github.com/acidanthera "acidanthera's GitHub Repo") for AppleALC.kext and Lilu.kext
- [**corpnewt**](https://github.com/corpnewt "CorpNewt's GitHub Repo") for the audio tutorial
- [**netkas**](https://www.netkas.org "netkas's Blog") for FakeSMC.kext
- [**RehabMan**](https://www.github.com/rehabman "RehabMan's GitHub Repo") for RealtekRTL8111.kext
- [**Timo**](https://www.github.com/timocapa "Timo's GitHub Repo") for putting up with me
- [**vit9696**](https://www.github.com/vit9696 "vit9696's GitHub Repo") for Shiki.kext and WhateverGreen.kext

❤️
