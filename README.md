# coreos-vagrant-for-windows-7
Initial working version of installing coreos-vagrant on Windows 7 with folder share support

1	Background
Being frustrated trying to get a quick working environment for CoreOS and was intrigued by the claim that using Vagrant would allow CoreOS run on a laptop initiated this foray.  The problem is that most of the documentation out there is focused on the Linux / Apple communities and those of us coming from the Windows community are quite a bit behind the curve in familiarization and support.  We are all on the bleeding edge of this technology so we will take quite a few bumps and more so being the redheaded step child.  
Note:  At least a month of playing with CoreOS, Docker and RancherOS on a VMWare ESX 5.5 and Hyper-V 2008R2 that was upgraded to Hyper-V 2012R2 has been conducted before this venture into coreos-vagrant.  Having to play DEV-OPS and have less time to explore CoreOS / Docker is a source of frustration.   CoreOS-Vagrant working on Windows 7 was not straight forward and much time and effort in researching a path through the set up prevents the Docker playground time.
This document is to assist other early adopters to join the fun of getting CoreOS clusters working with some Docker applications on existing equipment.  Hopefully you will find this document useful in aiding your path to a creating a cluster on your Windows laptop that wasn’t downloaded from Microsoft 
Read all of this information because it is required.  Skips may be suggested where possible.  Assume that you select default install paths for all packages.  

1.1	Strongly Suggested Before You Start
You have a 64 bit processor.  Were never successful getting CoreOS to run under 32bit Ubuntu 14 OS.
You have a GitHub account https://github.com/join and have the GitHub desktop installed on your machine https://desktop.github.com/ which will allow you to perform the steps below.
Have Putty (or other SSH client) installed on your machine and be familiar with PuTTYgen and the PuTTY client.  However, if you have a preferred SSH client that you use and know how to install SSH keys then use that.  There is no restriction on the SSH client.  
This document does not contain all setup steps.  References to other works are suggested in place and a list of sources is provided at the end for your own research and interpretation.

1.1.1	Packages Used
To accomplish this install the following packages have been used.
•	Vagrant
•	VirtualBox
•	GitHub Desktop
•	PuTTY
•	Cygwin  (MinGW is an alternative  
•	but it was not used here)

1.1.2	Host System Tested 
Dell Precision M6800, Windows 7 Pro, 6.1.7601 Service Pack 1 Build 7601, x64-based PC, Intel® Core™ i7-4900MQ CPU @ 2.80GHz, 2801 Mhz, 4 Core(s), 8 Logical Processor(s), BIOS Dell Inc. A09, 6/26/14, 16.0 G Physical Memory
