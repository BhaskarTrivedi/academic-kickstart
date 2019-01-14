+++
title = "How to install Tensorflow on ubuntu 16.04 server with GEForce RTX 2080" 
date = 2018-12-28T00:00:00

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["Bhaskar Chandra Trivedi"]

#List format.
#0 = Simple
#1 = Detailed
#2 = Stream
list_format = 2

# Tags (optional).
#   Set `tags = []` for no tags, or use the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags = ["Installation","Tensorflow"]


#Optional featured image (relative to static/img/ folder).
[header] 
image = "" 
caption = "" 
+++
1. [Download nomachine](https://www.nomachine.com/download).<br/>
2. Install nomachine<br/>
&nbsp;  &nbsp;  &nbsp; - On windows<br/>
&nbsp;  &nbsp;  &nbsp; &nbsp;  &nbsp;  &nbsp; - Run exe<br/>
&nbsp;  &nbsp;  &nbsp; - On Ubuntu<br/>
&nbsp;  &nbsp;  &nbsp; &nbsp;  &nbsp;  &nbsp; - sudo dpkg -i nomachine_XXXXX.deb ( your deb package name)<br/>
3. Configure nomachine to connect to server<br/>
&nbsp;  &nbsp;  &nbsp; - start nomachine from application<br/>
{{< figure src="1_NoMachine.JPG" title="" >}}
&nbsp;  &nbsp;  &nbsp; - Click on new<br/>
{{< figure src="2_NoMachine.JPG" title="" >}}
&nbsp;  &nbsp;  &nbsp; - Click continue<br/>
&nbsp;  &nbsp;  &nbsp; - Enter host name you want to connect and click continue.<br/>
{{< figure src="3_NoMachine.JPG" title="" >}}
&nbsp;  &nbsp;  &nbsp; - Select authentication type ( I used password).<br/>
{{< figure src="4_NoMachine.JPG" title="" >}}
&nbsp;  &nbsp;  &nbsp; - Select connection type.<br/>
{{< figure src="5_NoMachine.JPG" title="" >}}
&nbsp;  &nbsp;  &nbsp; - Choose Name.<br/>
{{< figure src="6_NoMachine.JPG" title="" >}}
&nbsp;  &nbsp;  &nbsp; - Click to added machine icon.<br/>
&nbsp;  &nbsp;  &nbsp; - Enter username and password of server machine.<br/>
{{< figure src="7_NoMachine.JPG" title="" >}}
5. Create virtual env.<br/>
&nbsp;  &nbsp;  &nbsp;  - conda create -n worldmodel python=3.5.4 numpy=1.13.3<br/>
&nbsp;  &nbsp;  &nbsp;  - logout user(sometime required)<br/>
&nbsp;  &nbsp;  &nbsp;  - source activate worldmodel<br/>
6. install tensorflow.<br/>
&nbsp;  &nbsp;  &nbsp;  - pip install --upgrade pip<br/>
&nbsp;  &nbsp;  &nbsp;  - pip install --ignore-installed --upgrade https://storage.googleapis.com/tensorflow/linux/gpu/tensorflow_gpu-1.12.0-cp35-cp35m-linux_x86_64.whl
.<br/>
&nbsp;  &nbsp;  &nbsp;  - possible error<br/>
&nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  - mkl-random 1.0.1 requires cython, which is not installed.<br/>
&nbsp;  &nbsp;  &nbsp;  - Install cython<br/>
&nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  - pip install --upgrade pip<br/>
&nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  - pip install cython<br/>
7. Verify Tensorflow installation.<br/>
&nbsp;  &nbsp;  &nbsp;  - python<br/>
&nbsp;  &nbsp;  &nbsp;  - import tensorflow<br/>
&nbsp;  &nbsp;  &nbsp;  - If installtion fail import will throw some error msg.<br/>
