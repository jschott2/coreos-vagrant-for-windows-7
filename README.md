# coreos-vagrant-for-windows-7
Initial save of Windows 7 coreos-vagrant

1	Background
Being frustrated trying to get a quick working environment for CoreOS and was intrigued by the claim that using Vagrant would allow CoreOS run on a laptop initiated this foray.  The problem is that most of the documentation out there is focused on the Linux / Apple communities and those of us coming from the Windows community are quite a bit behind the curve in familiarization and support.  We are all on the bleeding edge of this technology so we will take quite a few bumps and more so being the redheaded step child.  
Note:  At least a month of playing with CoreOS, Docker and RancherOS on a VMWare ESX 5.5 and Hyper-V 2008R2 that was upgraded to Hyper-V 2012R2 has been conducted before this venture into coreos-vagrant.  Having to play DEV-OPS and have less time to explore CoreOS / Docker is a source of frustration.   CoreOS-Vagrant working on Windows 7 was not straight forward and much time and effort in researching a path through the set up prevents the Docker playground time.
This document is to assist other early adopters to join the fun of getting CoreOS clusters working with some Docker applications on existing equipment.  Hopefully you will find this document useful in aiding your path to a creating a cluster on your Windows laptop that wasn’t downloaded from Microsoft 
Read all of this information because it is required.  Skips may be suggested where possible.  Assume that you select default install paths for all packages.  
1.1	Strongly Suggested Before You Start
You have a 64 bit processor.  Were never successful getting CoreOS to run under 32bit Ubuntu 14 OS.
You have a GitHub account https://github.com/join and have the GitHub desktop installed on your machine https://desktop.github.com/ which will allow you to perform the steps below.
Have Putty (or other SSH client) installed on your machine and be familiar with PuTTYgen and the PuTTY client.  However, if you have a preferred SSH client that you use and know how to install SSH keys then use that.  There is no restriction on the SSH client.  

WORK IN PROGREESS  9/1/2015

1	Background	
1.1	Strongly Suggested Before You Start
2	Running CoreOS on Vagrant	
2.1	Install Vagrant
2.2	Install VirtualBox	
2.3	Clone Vagrant Repo	
2.4	Starting a Cluster	
2.4.1	user-data	
2.4.2	config.rb	
2.4.3	Vagrantfile
2.4.4	Repeatable Launching of coreos-vagrant
2.4.5	Bring up the Cluster
2.4.6	Logging into the Guest Machines	
2.4.7	Find the insecure_private_key
2.4.7.1	Configure PuTTY to Use SSH Key
2.4.7.2	Connect to core-01	
2.4.7.3	Configure SSH Client and Connect to core-02 and core-03	
2.4.7.4	Information on the IP Addresses	
2.4.8	Review1:	
2.5	Shared Folders	
2.5.1	Notes on the VagrantFile Shared Folder Configuration Options
2.5.2	RSYNC:	
2.5.2.1.1	Installing CYGWIN
2.5.3	Set up for shared folders.
2.5.3.1	Hacking the helper.rb File	
2.5.4	Testing the Changes
2.5.5	Review2:
2.6	Getting Files from the Guest VM	
3	Research Links Used	

