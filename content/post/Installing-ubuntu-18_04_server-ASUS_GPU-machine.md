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
&nbsp;  &nbsp;  &nbsp;  &nbsp; e)Select free space from external drive to mount it -à Mostly followed at 1st time installation , don’t follow if you are updating OS in SSD and don’t want to lose data from external drive<br />
{{< figure src="/img/ExternalFreespace.jpg" title="" >}}

