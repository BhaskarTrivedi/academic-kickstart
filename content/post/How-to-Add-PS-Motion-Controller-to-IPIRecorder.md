+++
title = "How to Add PS Motion Controller to ipi Recorder" 
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
tags = ["Setup","PSMotionController"]

# Step to follow.
Desable_Secure_boot_in_ASUS_machine="1) Enter Boot Menu."
advancemenuimg=""


#Optional featured image (relative to static/img/ folder).
[header] 
image = "" 
caption = "" 
+++

1) Open ipi Recorder in Admin mode<br/>
2)Connect Motion Controller to PC through USB<br/>
3)Click on Add controller and select PlayStation Move<br/>
{{< figure src="/img/AddController.JPG"  >}}
<br/>
<br/>
2) It will try to pair with USB<br/>
{{< figure src="/img/PairingThroughUSB.JPG"  >}}
<br/>
<br/>
3) Disconnect from USB after you receive disconnect message<br/>
{{< figure src="/img/disconnectUSB.JPG"  >}}
<br/>
<br/>
4) Press PS button continuously, it will take few minutes<br/>
{{< figure src="/img/ClickPSButton.JPG"  >}}
<br/>
<br/>
5) Click on Add device when prompted<br/>
{{< figure src="/img/ClickAdddevice.JPG"  >}}
<br/>
<br/>
<br/>
<br/>
6) Click on Allow<br/>
{{< figure src="/img/AllowPairing.JPG"  >}}
<br/>
<br/>
<br/>
7) On successful pairing Connection Succeeded message will shown up<br/>
{{< figure src="/img/ConnectionSuccess.JPG"  >}}
<br/>
<br/>
<br/>
8) Motion Controller is paired with your computer
{{< figure src="/img/Paired.JPG"  >}}
<br/>
<br/>
<br/>
9)Motion controller should be visible to your ipi recorder.
{{< figure src="/img/ControllerAdded.JPG"  >}}

Troubleshoot
Sometime Motion controller is not visible into ipirecorder even after successful pairing. If it is not visible remove pairing from bluetooth device and repeat the step
