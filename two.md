# II - USB Drive

_"You should probably fully charge your Elitebook"_- Justin Case

---

## Ø - Partition & Format

_Now is the time to show me your trust, we're gonna have some CLI party time !_

- Launch a terminal
- Run `lsblk` and look for your USB drive's /dev/sdx  
  _for me it's /dev/sdf so I'll use that as reference, please change the `sdf` by the corresponding value_

- Run `sudo gdisk /dev/sdf`
  - Type `p` to check the current partitionning
    If it's the good one :
    - Type `o` to wipe the hell out of it.
      - Type `y` to confirm the shot.
  - Type `n` to create a new partition
    - Partition number: `Enter`
    - First Sector: `Enter`
    - Last Sector: `+200M` → `Enter`
    - Hex / GUID: `0700` → `Enter`
  - Type `p` to check that everything's as planned.  
    _You should have a single Microsoft Basic Data partition of 199/200Mb_
  - Type `n` again
    - Partition number: `Enter`
    - First Sector: `Enter`
    - Last Sector: `Enter`
    - Hex / GUID: `af00` → `Enter`
  - Type `p` to check everything.  
    _You should now have a new Apple HFS/HFS+ partition alongside the first one_

---

## I - GibMacOS & p7zip

_Now is the time to download the actual recovery image for our Live USB drive._

- Unzip gibMacOS and `cd` into it in your terminal.
- Run `./gibMacOS.command -r -v 10.14` or `python gibMacOS.command -r -v 10.14`
  _This will download the latest Recovery image for MacOS Mojave._

---

## II - Installation

!> TODO

- Run `sudo dd if=4.hfs of=/dev/sdf bs=8M`

---

## III - Adding Kexts

!> TODO

- Run `sudo mount /dev/sdf1 /mnt` and open your file explorer.
- Open the `/mnt` folder
- Copy and paste the EFI & Utilities folders in `/mnt`

---

## III - Finalizing

!> TODO


#### Your USB drive is now loaded with MacOS !

---

---

### Once all of this is done, you can jump into [Step 3](three.md)

---

@AktasC
2019 - 2020
