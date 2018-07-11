# High Sierra Clover Config Files for MSI Z97 PC MATE Motherboard.

### Introduction 
Once finalised, my personal Clover configuration files will be uploaded here.

I own **NONE** of the files that are supplied and all rights go to their original owners, I am merely sharing a combination of them for convinence of those who own the MSI Z97 PC MATE Motherboard. My PC is running macOS "High Sierra" 10.13.6 (17G65). It has an Intel i5-4690K paired with an AMD Radeon R9 390 running over DisplayPort.

### Working
- Full AMD Radeon R9 390 Support
  - You will have to patch a file for this to work, scroll down for tutorial

- Wired Networking

- Sleep/Wake

- USB 2

- FileVault

- Audio

### Not Working

- USB 3

### Untested
- WiFi

- Bluetooth

- Camera

- Microphone

### Patching AMDController8000.kext to support R9 390

1. Follow steps 5-12 of [this tutorial.](https://www.tonymacx86.com/threads/guide-getting-r9-290-390-non-x-to-work-on-sierra-10-12-and-high-sierra-10-13.210574/) Ignore the first section telling you to change your BIOS settings

2. Mount your EFI partition on Clover Configurator

3. Select the devices tab and under "Fake ID", enter '0x067B01002' into the ATI text-box

4. Select the graphics tab and type "Radeon" into the "FB Name" text-box, **make sure that "Inject ATI" is ticked**

5. Save your new config.plist file and make sure it's placed in 'EFI -> CLOVER -> config.plist'

6. Make sure that the latest versions of the AppleALC, Lilu and WhateverGreen kexts are present in your clover configuration

7. Reboot into macOS
