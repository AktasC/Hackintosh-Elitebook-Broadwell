## Ø - PREPARATION

### HARDWARE

- **A Desktop / Laptop running Linux**  
   _Ain't no Microsoft in my church unless it's a Surface device or for gaming._

- **An Ethernet Cable**  
   _You won't have Wi-Fi during the process._

- **USB Flash Drive** - at leat 12Gb  
   _USB 2.0 seems more stable but 3.0 works too._

- **HDD / SSD** SATA or mSATA  
   **_For NVMe drives you'll need a different guide._**

#### When you're finished gathering all that, download all of the following on your Mac :

### SOFTWARE

- **Bash**  
  _Sorry guys, you'll have to put fish/zsh aside for this guide for simplicity's sake_

- [gibMacOS](https://github.com/corpnewt/gibMacOS)  
  _This will allow us to create a MacOS Recovery Live USB_

- p7zip-full  
  _`sudo apt install p7zip-full` || `sudo pacman -Syu p7zip-full` || `sudo eopkg it p7zip` depending on your distro._

- [OpenCorePkg](https://github.com/acidanthera/OpenCorePkg/releases)
- [AppleCorePkg](https://github.com/acidanthera/AppleSupportPkg/releases)

- [HFSPlus.efi & HPFanReset.efi](https://bitbucket.org/RehabMan/hp-probook-4x30s-fan-reset/downloads/HPFanReset-2013-1205.efi.zip)

- [Config.plist](https://raw.githubusercontent.com/RehabMan/OS-X-Clover-Laptop-Config/master/config_HD5300_5500_6000.plist) Right click & Save as `config.plist`

### KEXTS

| Name                     | Link                                                                                           |
| ------------------------ | ---------------------------------------------------------------------------------------------- |
| VirtualSmc               | [VirtualSMC-x.x.x-RELEASE](https://github.com/acidanthera/VirtualSMC/releases)                 |
| IntelMausiEthernet.kext  | [OneDrive](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455134) |
| Lilu                     | [Lilu-x.x.x-RELEASE](https://github.com/acidanthera/Lilu/releases)                             |
| RealtekRTL8111.kext      | [OneDrive](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455143) |
| SATA-Unsupported.kext    | [OneDrive](https://github.com/RehabMan/hack-tools/archive/master.zip)                          |
| USBInjectAll.kext        | [OneDrive](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455146) |
| VoodooPS2Controller.kext | [OneDrive](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455152) |
| WhateverGreen            | [WhateverGreen-x.x.x-RELEASE](https://github.com/acidanthera/WhateverGreen/releases)           |

| For USB Tethering (optional) | 👇                                                                 |
| ---------------------------- | ------------------------------------------------------------------ |
| HoRNDIS                      | [Official Site](https://joshuawise.com/horndis#available_versions) |

---

## I - Structure everything

- Open your Downloads folder and unzip OpenCorePkg
- You should see three folders in the OpenCorePkg folder : `Docs`, `EFI` & `Utilities`.

We will now focus on the `EFI` folder.

- Unzip all the other archives you've downloaded and look at this structure :

```
|--EFI
   |   |--BOOT
   |   |   |--BOOTx64.efi
   |   |--OC (Main folder)
   |   |   |--ACPI
   |   |   |--Drivers
   |   |   |   |--ApfsDriverLoader.efi
   |   |   |   |--AppleUsbKbDxe.efi
   |   |   |   |--FwRuntimeServices.efi
   |   |   |   |--HPFanReset.efi
   |   |   |   |--NvmExpressDxe.efi
   |   |   |   |--VBoxHfs.efi
   |   |   |   |--XhciDxe.efi
   |   |   |--Kexts
   |   |   |   |--AppleALC.kext
   |   |   |   |--CPUFriend.kext
   |   |   |   |--IntelMausiEthernet.kext
   |   |   |   |--Lilu.kext
   |   |   |   |--RealtekRTL8111.kext
   |   |   |   |--SATA-unsupported.kext
   |   |   |   |--SMCBatteryManager.kext
   |   |   |   |--SMCLightSensor.kext
   |   |   |   |--SMCProcessor.kext
   |   |   |   |--SMCSuperIO.kext
   |   |   |   |--VirtualSMC.kext
   |   |   |   |--VoodooPS2Controller.kext
   |   |   |   |--WhateverGreen.kext
   |   |   |--Tools
   |   |   |   |--CleanNvram.efi
   |   |   |   |--VerifyMsrE2.efi
   |   |   |--OpenCore.efi
```

<small>Throw a coin to your InsanelyMacDiscord for the base snippet !</small>

- You need to place each element in it's corresponding folder.  
  _Pay attention to the file extension (`.kext` / `.efi`), some files may have the same name._  
  _You don't have to keep any .dsym or utility binary, **what you see is what you need** !_

---

---

### Once all of this is ready, you can finally jump into [Step 1](one.md)

---

@AktasC
2019 - 2020
