+++
title = "Installing Ubuntu 18.04 server ASUS GPU machine" 
date = 2018-12-21T00:00:00

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["Bhaskar Chandra Trivedi"]

#List format.
#0 = Simple
#1 = Detailed
#2 = Stream
list_format = 2

# Tags (optional).
#   Set `tags = []` for no tags, or use the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags = ["Server","Installation"]

# Step to follow.
Desable_Secure_boot_in_ASUS_machine="1) Enter Boot Menu."
advancemenuimg=""


#Optional featured image (relative to static/img/ folder).
[header] 
image = "" 
caption = "" 
+++
1)[Disable boot menu in ASUS machine](../disable-secure-boot-asus-machine)<br />
2)[Download Ubuntu 18.04LTS](http://cdimage.ubuntu.com/releases/18.04.1/release/?_ga=2.257800461.721767020.1545698526-895818190.1545698526)<br />
3)Creat bootable USB drive in UEFI mode( I used rufus software)<br />
4)Go to bios and keep USB drive (boot medium) at priority<br />
5)Save and exit<br />
6)Select Install Ubuntu Server<br />
7)Select all required option like language, country etc to next screen<br />
8)Select available network<br />
9)Enter Host name <br />
{{< figure src="/img/Host.jpg" title="" >}}
10)Enter user name and password<br />
11)Select partition type<br />
&nbsp;  &nbsp;  &nbsp;  &nbsp; a)Manual<br />
&nbsp;  &nbsp;  &nbsp;  &nbsp; b)Select SSD partition to install OS<br />
&nbsp;  &nbsp;  &nbsp;  &nbsp; c)Format the partition and go back<br />
&nbsp;  &nbsp;  &nbsp;  &nbsp; d)Select Guided partitioning<br />
{{< figure src="/img/GuidedPartition.jpg" title="" >}}
&nbsp;  &nbsp;  &nbsp;  &nbsp; e)Select free space from external drive to mount it Mostly followed at 1st time installation , don’t follow if you are updating OS in SSD and don’t want to lose data from external drive<br />
{{< figure src="/img/ExternalFreespace.jpg" title="" >}}
&nbsp;  &nbsp;  &nbsp;  &nbsp; f)Select space size to mount<br />
{{< figure src="/img/externalsize.jpg" title="" >}}
&nbsp;  &nbsp;  &nbsp;  &nbsp; g)Select done setting up the partition<br />
{{< figure src="/img/donepatition.jpg" title="" >}}
&nbsp;  &nbsp;  &nbsp;  &nbsp; h)Select finish partitioning and write changes to disk<br />
{{< figure src="/img/finishpartition.jpg" title="" >}}
12) Install Unity <br />
&nbsp;  &nbsp;  &nbsp;  &nbsp; a)sudo apt update<br />
&nbsp;  &nbsp;  &nbsp;  &nbsp; b)sudo apt install ubuntu-unity-desktop<br />
&nbsp;  &nbsp;  &nbsp;  &nbsp; c)sudo shutdown -r now<br />
13)Install the NVIDIA display driver <br />
&nbsp;  &nbsp;  &nbsp;  &nbsp; a)sudo add-apt-repository ppa:graphics-drivers/ppa<br />
&nbsp;  &nbsp;  &nbsp;  &nbsp; b)sudo apt-get update<br />
&nbsp;  &nbsp;  &nbsp;  &nbsp; c)sudo ubuntu-drivers devices<br />
&nbsp;  &nbsp;  &nbsp;  &nbsp; d)Check recommended version which need to install<br />
&nbsp;  &nbsp;  &nbsp;  &nbsp; e)sudo ubuntu-drivers autoinstall<br />
&nbsp;  &nbsp;  &nbsp;  &nbsp; f)sudo shutdown -r now<br />
&nbsp;  &nbsp;  &nbsp;  &nbsp; g)nvidia-smi<br />
14)Create New sudo user <br />
&nbsp;  &nbsp;  &nbsp;  &nbsp; a)Sudo adduser username<br />
&nbsp;  &nbsp;  &nbsp;  &nbsp; b)Sudo usermod -aG sudo username<br />
&nbsp;  &nbsp;  &nbsp;  &nbsp; c)Test sudo access<br />
&nbsp;  &nbsp;  &nbsp;  &nbsp; &nbsp;  &nbsp;  &nbsp;  &nbsp; A)su – username<br />
&nbsp;  &nbsp;  &nbsp;  &nbsp; &nbsp;  &nbsp;  &nbsp;  &nbsp; B)sudo whoami<br />
15) Troubshoot If got error msg “PKCS#7 signature not signed with a trusted key<br />
&nbsp;  &nbsp;  &nbsp;  &nbsp; a)Remove nvidia completely using purges/ppa<br />
&nbsp;  &nbsp;  &nbsp;  &nbsp; b)sudo apt remove nvidia-*<br />
&nbsp;  &nbsp;  &nbsp;  &nbsp; c)sudo apt purge nvidia*<br />
&nbsp;  &nbsp;  &nbsp;  &nbsp; d)sudo apt autoremove<br />
&nbsp;  &nbsp;  &nbsp;  &nbsp; e)sudo apt autoclean<br />
&nbsp;  &nbsp;  &nbsp;  &nbsp; f)sudo apt-get remove --purge libnvidia-compute-XXX:XXXX<br />
&nbsp;  &nbsp;  &nbsp;  &nbsp; g)sudo apt-get remove --purge libnvidia-compute-XXX<br />
&nbsp;  &nbsp;  &nbsp;  &nbsp; h)Make sudo dpkg -l | grep nvidia return empty<br />
&nbsp;  &nbsp;  &nbsp;  &nbsp; i)Install nvidia driver using autoinstall describe in step 13<br />

