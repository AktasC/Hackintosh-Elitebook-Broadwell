# Work In Progress

# Vanilla MacOS Mojave on an HP Elitebook 840 G2

Welcome on another Hackintosh guide !

This is a simple yet complete step by step guide on how to install MacOS Mojave on an HP Elitebook 840 G2.

--------------------------------------------------------------------------------

# DISCLAIMER

**Installing macOS on non-Apple hardware is a violation of their EULA.<br>
This is intended as an experiment and will most likely not suit your needs as a daily driver.**

Keep in mind that all of this is **experimental** and Apple could _end it_ at **any version.**<br>
_(Always make a backup before updating, you never know.)_

**Neither me nor the contributors are responsible if anything happens to you, your devices, Flash Drives, Laptop's components or anything else.**<br>
**You're the sole responsible for what you do** and **SHOULD** do your research before _blindly_ following any guide.

--------------------------------------------------------------------------------

## Quick facts & answers

- [x] _Why another f*ing guide ?_

- For no good reason honestly, I don't like the way [all those guides](https://www.tonymacx86.com/forums/mojave-laptop-guides.197/) are written & wanted to keep a summary / step by step guide for myself but then decided to share it here...<br>
  Sorry Nguyenmac, Rehabman & Spotflight, I read them a hundred times but it's really hard to understand how we got there, it feels like there's too much noise, _'useless'/generic_ info.<br>
  I think it's the forum that makes it _'less readable'_, the general look, font, structure... I don't know.<br>
  This guide will focus on doing the job instead of explaining every step, so there is that.

- [x] _Why this laptop ?_

- I had to buy it when I studied at Epitech Strasbourg, in France.<br>
  This specific laptop was mandatory & **absolutely not worth** the money.<br>
  _And this laptop is cursed... So... let it burn._

- [x] _Why a hackintosh ? Wasn't Linux enough of an adventure ?_

- Fair enough, Linux is a whole world to explore and it keeps expanding everyday.<br>
  The thing is, for around 5 to 6 years I've been able to experiment on Linux & Windows, but now I feel like I should also look at MacOS and other BSD based systems because it's _"different"_. Used to have colleagues with Macbooks and they definitely got their job done so why not give it a try ?<br>
  The problem was : giving it a try meant at least 700€ in cash (for the lowest config) and I don't have that 😂

- [x] _Do I risk anything ?_

- You could fry your Motherboard or CPU, corrupt your HDD / SSD, lose precious data if there are any, get sued by Apple, find yourself teleported into AREA 51 ..<br>
  I mean, anything is possible right ?

- [x] _Can I get the Wifi / Bluetooth card to work ?_

- The short answer is no.<br>
  The longer answer would be :<br>
  "Because Apple never used Intel Wifi cards, there's no support for them.<br>
  You could potentially swap your current card for one used by Apple.<br>
  A refurbished Broadcom BCM94352Z on AliHeck's Press should do the trick !"

--------------------------------------------------------------------------------

## Specs

- Intel **i7-5600U**
- Intel **HD 5500**
- Radeon R7 M260X _(Disabled)_
- Intel Wireless AC-7265 _(disabled)_
- 8Gb DDR3 @ 1600MHz
- 14"- 1920*1080
- 500Gb HDD - SATA

If your laptop isn't the exact same one you should look for a guide _specifically featuring **yours.**_<br>
Hackintosh guides are "kinda" vanilla but this one will really focus on the Broadwell i7 equipped HP Elitebook 840 G2.

--------------------------------------------------------------------------------

## Ø - PREPARATION

### HARDWARE

- [x] **A legit Apple device running MacOS**. _Can be a Mac Mini, Macbook (Pro), iMac, iWhatever._<br>
  _Don't use a VM for this, you'll waste your time, but a Hackintosh would work lmao_
- [x] **An Ethernet Cable**<br>
  _You won't have Wi-Fi_
- [x] **USB Flash Drive** - at leat 8Gb<br>
  _USB 2.0 seems more stable but 3.0 works too_
- [x] **HDD / SSD** SATA or mSATA<br>
  **_For NVMe drives you'll need a different guide._**

#### When you're finished gathering all that, download all of the following on your Mac :

### SOFTWARE

- [x] [Clover Installer](https://sourceforge.net/projects/cloverefiboot/files/Installer/)
- [x] [HFSPlus.efi & HPFanReset.efi](https://bitbucket.org/RehabMan/hp-probook-4x30s-fan-reset/downloads/HPFanReset-2013-1205.efi.zip)
- [x] [Config.plist](https://raw.githubusercontent.com/RehabMan/OS-X-Clover-Laptop-Config/master/config_HD5300_5500_6000.plist) Right click & Save as `config.plist`
- [x] [MacOS Mojave](https://apps.apple.com/fr/app/macos-mojave/id1398502828?mt=12)

### KEXTS

Centralized Kext Repo                                   | Link
------------------------------------------------------- | --------------------------------------------------------------
This is a drive where you'll find most vanilla kexts    | [OneDrive](https://1drv.ms/f/s!AiP7m5LaOED-m-J8-MLJGnOgAqnjGw) |
Always nice to keep in case you want to update anything | ☝️ Bookmark this                                             |

Name                         | Link
---------------------------- | ----------------------------------------------------------------------------------------------
FakeSMC.kext                 | [OneDrive](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455161) |
IntelMausiEthernet           | [OneDrive](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455134) |
Lilu.kext                    | [OneDrive](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455053) |
RealtekRTL8111.kext          | [OneDrive](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455143) |
SATA-Unsupported.kext        | [OneDrive](https://github.com/RehabMan/hack-tools/archive/master.zip)                          |
USBInjectAll.kext            | [OneDrive](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455146) |
VoodooPS2Controller.kext     | [OneDrive](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455152) |
WhateverGreen.kext           | [OneDrive](https://onedrive.live.com/?authkey=%21APjCyRpzoAKp4xs&id=FE4038DA929BFB23%21455095) |
For USB Tethering (optional) | 👇                                                                                             |
HoRNDIS                      | [Official Site](https://joshuawise.com/horndis#available_versions)

--------------------------------------------------------------------------------

### Once all of this is ready, you can jump into [Step 1](/I-BIOS/README.md)

--------------------------------------------------------------------------------

# Credits

First of all, sorry for not providing your repos in the download sections.<br>
I knew the drive was automagically kept up-to-date so I decided to go with a centralized source.

I've never been good at thanking people but here we go :

- [Acidanthera](https://github.com/acidanthera/) - **Illuminati** Can't say much more... Thanks for your work guys !
- [NguyenMac](https://www.tonymacx86.com/members/nguyenmac.598852/) - **Guide Senpai** For creating and maintaining the guide I used to follow for so long, contributed to turn me into a _mad_ SysAdmin.
- [Rehabman](https://github.com/rehabman) - **Laptop Guru** Guides, configs, kexts, SSDTS, ~drugs,~ **you name it**. This guy has 'em all !
- [Spotflight](https://www.tonymacx86.com/members/spotflight.1654314/) - **Elitebook Chief** For his simplified / modernized guide which helped me avoid some obsolete tricks I used to use.
- Every single other contributor, developer, pioneer who helped achieve all of this.
- _Coffee & poverty made me do it_.

@AktasC - 2019
