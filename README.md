# slackrock
This is a set of scripts I have been using to create a disk image and public images I have created off the current rock64 ayufan kernel and combined with Slackware Arm Current.

Install Instructions:

0) Download the latest slackware armhf release.
   
1) As a privileged user please run:
   zcat slackware-armhf*img | sudo dd of=/dev/sdX status=progress
   
2) I have not created a script to autoexpand the drive so this must be done with gparted.

3) After boot you can login with user user: rock64 and pass: rock64 
   this user has sudo access.
