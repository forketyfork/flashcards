START
Basic
Front: 
When running Ubuntu in a VM, how to solve an error "Release file is not valid yet", similar to: `Release file for http://ports.ubuntu.com/ubuntu-ports/dists/jammy-updates/InRelease is not valid yet (invalid for another 1min 17s). Updates for this repository will not be applied`?
Back: 
Run this command to sync your VM time with your host, it sets system clock from the hardware clock.
```
sudo hwclock --hctosys
```
<!--ID: 1745139755258-->
END
