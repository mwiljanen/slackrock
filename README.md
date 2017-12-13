# slackrock
This is a set of scripts I have been using to create a disk image and public images I have created off the current rock64 ayufan kernel and combined with Slackware Arm Current.

Install Instructions:

0) Download the latest slackware armhf release https://github.com/mwiljanen/slackrock/releases
   
1) As a privileged user please run:
   zcat slackware-current-minimal-rock64-0.5.10-118-armhf.img.gz | sudo dd of=/dev/sdX bs=4M status=progress
   
2) I have not created a script to autoexpand the drive so this must be done with gparted.

3) After boot you can login with user user: rock64 and pass: rock64 
   this user has sudo access.
   
4) To get this image on the internet you must use ifconfig or dhcpcd with an ethernet cable, Network manager is not installed on the slackware-minimal rootfs.

5) After you get a connection to the internet now you can install all the packages, but do not install the slackwarearm-current kernels, you can blacklist these in the /etc/slackpkg/blacklist.  If you install this kernel your rock64 will refuse to boot.
To upgrade do these steps:

  * slackpkg update
  * slackpkg install-new
  * slackpkg upgrade-all

  This upgrade will take over an hour or more, so please be patient and if you do the full install it will be about +9GB of space on your SD card so a 16GB card is not recommended for a full install.
  
  Now you can enjoy slackware on you Rock64!
  
  Enjoy!
  
  Matt
