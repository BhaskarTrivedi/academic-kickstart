+++
title = "Image Derivation" 
date = 2019-09-13T00:00:00

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["Bhaskar Chandra Trivedi"]

#List format.
#0 = Simple
#1 = Detailed
#2 = Stream
list_format = 2

# Tags (optional).
#   Set `tags = []` for no tags, or use the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags = ["Computer Vision"]

# Step to follow.
Desable_Secure_boot_in_ASUS_machine="1) Enter Boot Menu."
advancemenuimg=""


#Optional featured image (relative to static/img/ folder).
[header] 
image = "" 
caption = "" 
+++
When I started computer vision the most common term, I found was Image derivation. In my school I learned derivation on the function, but the images are collection discreet value in terms of pixel. Its value ranges from 0 to 255   in terms of intensity. How can we apply derivative to discrete value it is not some function? Initially, I was confused and spend lots of time to figured out what exactly it means. With more digging I found Image differentiation refer to different to its pixel value.
It has three ways to calculate differentiation <br />
df/dx = f(x) – f(x-1) = f’(x)                   backward difference<br />
df/dx= f(x) – f(x+1) = f’(x)                    forward difference<br />
df/dx= f(x+1) – f(x+1) = f’(x)                  Central difference<br />
 
[10	20	10	200	210	250	250]<br />

Central derivative [ -1 0 1]<br />
Derivative at index 3 = 210 – 10 = 200<br />
Derivative mask for image<br />

{{< figure src="/img/ID1.JPG" title="" >}}<br />

derivative<br />

{{< figure src="/img/ID2.JPG" title="" >}}<br />

Example given in shah lecture with x and y derivative <br />
{{< figure src="/img/ID3.JPG" title="" >}}<br />

Reference <br/>
https://mccormickml.com/2013/02/26/image-derivative/ <br />
https://www.youtube.com/watch?v=1THuCOKNn6U <br />
http://www.cs.cmu.edu/~16385/s17/Slides/4.0_Image_Gradients_and_Gradient_Filtering.pdf <br />
