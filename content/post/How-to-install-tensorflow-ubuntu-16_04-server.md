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
1. [Install cuda 9.0 without nvidia driver](https://developer.nvidia.com/cuda-90-download-archive?target_os=Linux&target_arch=x86_64&target_distro=Ubuntu&target_version=1604&target_type=runfilelocal).<br/>
&nbsp;  &nbsp;  &nbsp;  - sudo chmod +x cuda_9.0.176_384.81_linux.run<br/>
&nbsp;  &nbsp;  &nbsp;  - sudo ./cuda_9.0.176_384.81_linux.run --extract=/home/username/Dirname<br/>
&nbsp;  &nbsp;  &nbsp;  - sudo ./cuda-linux.9.0.176-22781540.run<br/>
&nbsp;  &nbsp;  &nbsp;  - sudo ./cuda-samples.9.0.176-22781540-linux.run<br/>
&nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  - install patch 1<br/>
&nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  - [download patch 1](https://developer.nvidia.com/cuda-90-download-archive?target_os=Linux&target_arch=x86_64&target_distro=Ubuntu&target_version=1604&target_type=runfilelocal)<br/>
&nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  - sudo sh cuda_9.0.176.1_linux.run<br/>
&nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  - [download patch 2](https://developer.nvidia.com/cuda-90-download-archive?target_os=Linux&target_arch=x86_64&target_distro=Ubuntu&target_version=1604&target_type=runfilelocal)<br/>
&nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  - sudo sh cuda_9.0.176.2_linux.run<br/>
&nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  - [download patch 3](https://developer.nvidia.com/cuda-90-download-archive?target_os=Linux&target_arch=x86_64&target_distro=Ubuntu&target_version=1604&target_type=runfilelocal)<br/>
&nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  - sudo sh cuda_9.0.176.3_linux.run<br/>
&nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  - [download patch 4](https://developer.nvidia.com/cuda-90-download-archive?target_os=Linux&target_arch=x86_64&target_distro=Ubuntu&target_version=1604&target_type=runfilelocal)<br/>
&nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  - sudo sh cuda_9.0.176.4_linux.run<br/>
2.set cuda path variable<br/>
&nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  - sudo cp ~/.bashrc ~/.bashrc_backup<br/>
&nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  - sudo nano ~/.bashrc<br/>
&nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  - export PATH="/usr/local/cuda-9.0/bin:$PATH"<br/>
&nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  &nbsp;  - export LD_LIBRARY_PATH="/usr/local/cuda-9.0/lib64:$LD_LIBRARY_PATH"<br/>
3. Install required cuDNN SDK for cuda 9.0.<br/>
4. [Download Anaconda and install Anaconda3-2018.12-Linux-x86_64.](https://www.anaconda.com/download/#linux)<br/>
&nbsp;  &nbsp;  &nbsp;  - sudo bash Anaconda3-2018.12-Linux-x86_64.sh.<br/>
&nbsp;  &nbsp;  &nbsp;  - sudo shutdown -r now.<br/>
5. Create virtual env.<br/>
&nbsp;  &nbsp;  &nbsp;  - conda create -n worldmodel python=3.6.8 numpy=1.13.3<br/>
&nbsp;  &nbsp;  &nbsp;  - logout user(sometime required)<br/>
&nbsp;  &nbsp;  &nbsp;  - source activate worldmodel<br/>
6. install tensorflow.<br/>
&nbsp;  &nbsp;  &nbsp;  - pip install --upgrade pip<br/>
&nbsp;  &nbsp;  &nbsp;  - pip install --ignore-installed --upgrade https://storage.googleapis.com/tensorflow/linux/gpu/tensorflow_gpu-1.12.0-cp36-cp36m-linux_x86_64.whl
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
