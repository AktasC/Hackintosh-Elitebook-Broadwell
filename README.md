# Work In Progress

## Vanilla MacOS Mojave on an HP Elitebook 840 G2 {docsify-ignore}

Welcome on another Hackintosh guide !

This is a simple yet complete step by step guide on how to install MacOS Mojave on an HP Elitebook 840 G2.

---

## DISCLAIMER

!> Installing MacOS on non-Apple hardware is a violation of their EULA.  
This is intended as an experiment and will most likely not suit your needs as a daily driver.

Keep in mind that all of this is **experimental** and Apple could _end it_ at **any version.**  
_(Always make a backup before updating, you never know.)_

**Neither me nor the contributors are responsible if anything happens to you, your devices, Flash Drives, Laptop's components or anything else.**  
**You're the sole responsible for what you do** and **SHOULD** do your research before _blindly_ following any guide.
<small>Says the guy who writes a publicly available simplified guide about installing MacOS on non-Apple hardware... You've been warned.</small>

---

## Quick facts & answers

- _Why another f\*ing guide ?_

  - For no good reason honestly, I don't like the way [all those guides](https://www.tonymacx86.com/forums/mojave-laptop-guides.197/) are written & wanted to keep a summary / step by step guide for myself but then decided to share it here...  
    Sorry Nguyenmac, Rehabman & Spotflight, I read them a hundred times but it's really hard to understand how we got there, it feels like there's too much noise, _'useless'/generic_ info.  
    I think it's the forum that makes it _'less readable'_, the general look, font, structure... I don't know.  
    This guide will focus on doing the job instead of explaining every step, so there is that.

- _Why this laptop ?_

  - I had to buy it when I studied at Epitech Strasbourg, in France.  
     This specific laptop was mandatory & **absolutely not worth** the money.  
    _And this laptop is cursed... So... let it burn._

- _Why a hackintosh ? Wasn't Linux enough of an adventure ?_

  - Fair enough, Linux is a whole world to explore and it keeps expanding everyday.  
    The thing is, for around 5 to 6 years I've been able to experiment on Linux & Windows, but now I feel like I should also look at MacOS and other BSD based systems because it's _"different"_. Used to have colleagues with Macbooks and they definitely got their job done so why not give it a try ?  
    The problem was : giving it a try meant at least 700€ in cash (for the lowest config) and I don't have that 😂

- _Do I risk anything ?_

  - You could fry your Motherboard or CPU, corrupt your HDD / SSD, lose precious data if there are any, get sued by Apple, find yourself teleported into AREA 51 ..  
    I mean, anything is possible right ?

- _Can I get the Wifi / Bluetooth card to work ?_

  - The short answer is no.  
    The longer answer would be :  
    "Because Apple never used Intel Wifi cards, there's no support for them.  
    You could potentially swap your current card for one used by Apple.  
    A refurbished Broadcom BCM94352Z on AliHeck's Press should do the trick !"

---

## Specs

- Intel **i7-5600U**
- Intel **HD 5500**
- Radeon R7 M260X _(Disabled)_
- Intel Wireless AC-7265 _(disabled)_
- 8Gb DDR3 @ 1600MHz
- 14"- 1920\*1080
- 500Gb HDD - SATA

?> If your laptop isn't the exact same one you should look for a guide _specifically featuring **yours.**_  
Even though Hackintosh guides are mostly generic, this one will really focus on the Broadwell i7 equipped HP Elitebook 840 G2.
<small>(It should work if you happen to have an HD5300/5500/6000 iGPU but I'd rather not encourage any fool...)</small>

---

---

### So you've read all the warnings, checked your hardware and prepared yourself to die ? Enter [Step 0](zero.md)

---

@AktasC
2019 - 2020
