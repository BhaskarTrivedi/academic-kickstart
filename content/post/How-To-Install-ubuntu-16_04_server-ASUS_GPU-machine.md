+++
title = "How to install Ubuntu 16.04 server ASUS GPU machine" 
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
2)[Download Ubuntu 16.04LTS](http://releases.ubuntu.com/16.04/)<br />
3)Creat bootable USB drive in UEFI mode( I used rufus software)<br />
{{< figure src="/img/ubuntu_1604_28.JPG" title="" >}}
4)Go to bios and keep USB drive (boot medium) at priority<br />
5)Save and exit<br />
6)Select Install with the HWE kernel<br />
{{< figure src="/img/ubuntu_1604_1.JPG" title="" >}}
7)Select Install ubuntu server<br />
{{< figure src="/img/ubuntu_1604_2.JPG" title="" >}}
8)Select all required option like language, country etc to next screen<br />
9)Enter host Name<br />
{{< figure src="/img/ubuntu_1604_3.JPG" title="" >}}
10)Enter user name and password<br />
{{< figure src="/img/ubuntu_1604_4.JPG" title="" >}}
11)Unmount partition (These steps are for fresh installation from scratch, don’t follow if you don’t want to format your data)<br />
{{< figure src="/img/ubuntu_1604_5.JPG" title="" >}}
12)Select manual partition<br />
13)Select partition and create new partition<br />
{{< figure src="/img/ubuntu_1604_6.JPG" title="" >}}
