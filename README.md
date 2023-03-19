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
`cryptsetup lukFormat /dev/{device} {nameOfReference}`
3. Create directory for boot
`mkdir boot`
4. mount your boot first!!!
`mount /dev/nvme-n1p1 /root/boot`
5. mount the /root
`mount /dev/{devicename} /root`
or 
`mount /dev/mapper/{deviceName} /root`
![alt text](https://github.com/WilliamPring/ArchLinuxRescueGuide/blob/main/images/lsblk(before-arch-chroot).jpg)


