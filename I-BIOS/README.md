# I - BIOS

Before installing MacOS we have to set our BIOS properly.<br>
It needs to look "fresh outta factory" so let's clean that up !

--------------------------------------------------------------------------------

## Ø - Enter BIOS Menu

- Your laptop needs to have AC and Ethernet connected.
- Boot it up.
- Press `F10` on boot.<br>
  If you're late, press `CTRL + ALT + DEL` and retry.

## I - Update your BIOS

- **Main Tab**
- Update system BIOS
  - Check HP.com for BIOS Updates
- Let it install & reboot (approx 3mn)

## II - Restore default settings

- [Enter BIOS menu](#0---enter-bios-menu)
- **Main Tab**
- Restore Defaults
  - Yes
- Reboot

## III - Set the BIOS for MacOS

Since whe restored the default settings, we will only need to change a handful of settings.<br>
If what I check is already checked or what I uncheck is already unchecked : let it be.<br>
All we need is to have the same options enabled and disabled, don't touch anything unless you know what you're doing.<br>
You'll have plenty of time to tweak and play with them **once it works**.<br>

Here we go then :

- [Enter BIOS menu](#0---enter-bios-menu)
- **Advanced tab**
- Boot Options
  - Startup Menu Delay (Sec.) : **05**
  - [ ] Fast Boot
  - [x] USB Device boot
  - [x] PCIe/M.2 SSD boot
  - Boot Mode : UEFI Hybrid (With CSM)
- Device Configurations
  - [x] USB legacy support
  - [x] USB 3.0 (HXCI)
  - Video Memory Size : **64MB**
  - [ ] Wake on USB
  - [ ] Virtualization (VTx / VTd)
  - [ ] Trusted Execution Technology (TXT)
  - [ ] Hybrid Graphics
  - [x] Deep sleep
- Built-in Device Options
  - Wake on LAN : **Disable**
  - [x] Wake unit from sleep when lid is opened
  - [x] Power on unit when lid is opened
  - [x] PCIe/M.2 SSD
- Port Options
  - [x] USB port
  - [ ] Smart Card
- **Main Tab**
- Save Changes and Exit
