# Are You About To Do Tech Support?
Someone you know (or you!) has a technical problem. This document details a few starting points for what to do and what not to do.

## Rules if you are receiving tech support
* Do not ever under any circumstances snap at the person or people trying to help you. Computer shit is frustrating, and especially when you have to basically play charades with someone a thousand miles away, but it discourages people from helping you if you shout at them.
*  Don't assume you're being condescended to if asked to perform certain debugging tasks or asked if you've done things you consider to be trivial or things you've already done. Reacting to these kind of things negatively makes it more likely that the person providing help may skip another critical debugging step, not wanting to annoy you and hoping you've already done it.

## Rules if you are giving tech support
* No needless condescension. Don't freak out when people don't know shit. "you don't know what a CPU is!?" is not a way to endear yourself to the person you're helping.
* Try your best not to talk out of your ass. If you don't know something, use google or fess up. This applies less for lower stakes stuff and more for things like recommending new hardware, overclocking, etc.


## Software recommendations
[HWMonitor](https://www.cpuid.com/softwares/hwmonitor.html) - shows temperatures and other important metics like fan speeds
[NVIDIA App](https://www.nvidia.com/en-us/software/nvidia-app/) - use this instead of GeForce Experience

## Precautions for PC use
Are you a one-PC household? Make sure to make a Linux bootable USB stick.
Any distro will do, but if you're unsure, just grab Linux Mint using [unetbootin](https://unetbootin.github.io/)

This is useful in case your OS installation gets corrupted.


## Issues

### Overheating
Is your PC running slow? Are you hitting temperatures of 75 or higher? Investigate core frequencies on CPU and GPU. If it is dipping, that might be why.
Step 1: Clean your case and radiators for dust.
Step 2: If problem persists for CPU, apply new thermal paste on CPU.
Step 3: If problem still persists, ping the role, probably get a new cooler.

### Sources of instability that aren't always talked about
* Outdated BIOS.
* Improperly connected USB devices (symptoms range from videos not playing properly to complete system crashes).
* Corrupted Windows installation from a crash. The following commands run as admin in cmd may help fix issues:
```
sfc /scannow 
DISM.exe /Online /Cleanup-image /Scanhealth
DISM.exe /Online /Cleanup-image /Restorehealth
DISM.exe /Online /Cleanup-image /startcomponentcleanup
```
