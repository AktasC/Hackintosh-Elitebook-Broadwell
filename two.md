# II - USB Drive

Grab your Mac & your USB drive, put your Elitebook away and let's create a bootable USB.
_"You should probably charge up your Elitebook"_- Justin Case

---

## Ø - Preparation

- Launch a terminal
- `diskutil list`
- You need your **USB DRIVE'S** `IDENTIFIER` must look like `disk1`
  - Double check it's the good one and not your HDD.
- `diskutil partitionDisk /dev/IDENTITIFER 2 MBR FAT32 "CLOVER" 200Mi HFS+J "INSTALL" R`
  - Double check you've replaced `IDENTIFIER` with the proper `diskX` before pressing ENTER

You should have a brand new USB stick named CLOVER

---

## I - Installation

- Run the Clover installer you downloaded earlier
- Next
- Click on `Change Installation Location` and set it on `CLOVER`
- Select `Customize`
  - [x] Install for UEFI booting only
  - [x] Install Clover in the ESP
- 64Bit Drivers
  - [x] AptioMemoryFix
  - [x] ApfsDriverLoader
  - [x] AudioDxe
  - [x] FSInject
  - [x] SMCHelper
  - [x] VBoxHfs
- Install
- _Grab a cup of coffee_
- Close the Clover installer
- Copy `HFSPlus.efi` & `HPFanReset.efi` to `/Volumes/CLOVER/EFI/CLOVER/drivers/UEFI/`

---

## II - Adding Kexts

- Open a Finder in `/Volumes/CLOVER/EFI/CLOVER/kexts/Other/`
- Copy and paste these kexts in that folder :
  - `FakeSMC.kext`
  - `Lilu.kext`
  - `IntelMausiEthernet.kext`
  - `RealtekRTL8111.kext`
  - `SATA-unsupported.kext`
  - `USBInjectAll.kext`
  - `VoodooPS2Controlleer.kext`
  - `WhateverGreen.kext`
- Open the `config.plist` you downloaded earlier
- Delete this part of the file :

```XML
    <key>DVMT-prealloc</key>
    <string>32MB BIOS, 19MB framebuffer, 9MB cursor bytes (credit RehabMan)</string>
    <key>framebuffer-patch-enable</key>
    <integer>1</integer>
    <key>framebuffer-stolenmem</key>
    <data>AAAwAQ==</data>
    <key>framebuffer-fbmem</key>
    <data>AACQAA==</data>
```

  - Save & Close
- Copy your `config.plist` to `/Volumes/CLOVER/EFI/CLOVER/` (replace the old one)

---

## III - Finalizing

- Start a terminal
- `sudo /Applications/Install\ macOS\ Mojave.app/Contents/Resources/createinstallmedia --volume /Volumes/INSTALLER`
  - Input your password when asked to
  - Press `y` to confirm
- Close the terminal when it's done
- Eject the USB drive

#### Your USB drive is now loaded with MacOS !

---

### Once all of this is ready, you can jump into [Step 3](three.md)

---

@AktasC
2019 - 2020
