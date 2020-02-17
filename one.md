# I - BIOS

Before installing MacOS we have to setup our BIOS properly.  
It needs to look "fresh outta factory" so let's clean that up !

---

## Ø - Enter BIOS Menu

- Plug in the AC & Ethernet.
- Power on the Elitebook.
- Smash `F10` like your life depends on it.

?> If you're late, press `CTRL + ALT + DEL` and retry.

---

## I - Update your BIOS

- **Main Tab**
  - Update system BIOS
    - Check HP.com for BIOS Updates
- Let it install & reboot (~ 3-5mn)

---

## II - Restore default settings

- [Enter BIOS menu](/one?id=%c3%98-enter-bios-menu)
- **Main Tab**
  - Restore Defaults
    - Yes
- Reboot

---

## III - Set the BIOS for MacOS

Since whe restored the default settings, we will only need to change a handful of settings.  
If what I check is already checked or what I uncheck is already unchecked : let it be.  
All we need is to have the same options enabled and disabled, **don't touch anything unless you know what you're doing.**  
You'll have plenty of time to tweak and play with them **once it works**.

Here we go then :

- [Enter BIOS menu](/one?id=%c3%98-enter-bios-menu)
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
- Poweroff your laptop.

#### Your Elitebook is now ready for MacOS !

---

---

### Once all of this is ready, you can jump into [Step 2](two.md)

---

@AktasC - 2019
