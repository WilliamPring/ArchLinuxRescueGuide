# ArchLinuxRescueGuide
Just a guide for myself to refer to when I cannot boot into my machine


## GUIDE TO Mount your drive 

### Initialization
1. Get the ISO: https://archlinux.org/download/

2. Run the command
`lsblk`


3. Mount the ISO on your usb: 


### Boot to usb
1. Boot into the usb
2. Decrpyt the drive for home or boot. Do it both if you need to
`cryptsetup open /dev/{device} {nameOfReference}`
3. Create directory for boot
`mkdir boot`
4. mount your boot first!!!
`mount /dev/nvme-n1p1 /root/boot`
5. mount the /root
`mount /dev/{devicename} /root`
or 
`mount /dev/mapper/{deviceName} /root` 
6. `lsblk`
Should look like this:
![alt text](https://github.com/WilliamPring/ArchLinuxRescueGuide/blob/main/images/lsblk(before-arch-chroot).jpg)
7. after mounting the drive chroot into your machine
`arch-chroot /root`
8. You should be in your machine and it should look like this:
![alt text](https://github.com/WilliamPring/ArchLinuxRescueGuide/blob/main/images/lsblk(after-arch-chroot).jpg)
9. From here you can downgrade your kernal, etc. Refer to this: https://wiki.archlinux.org/title/downgrading_packages

```
pacman -U file:///var/cache/pacman/pkg/package-old_version.pkg.tar.type
``` 

