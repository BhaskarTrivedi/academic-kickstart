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
tags = ["Development"]


#Optional featured image (relative to static/img/ folder).
[header] 
image = "" 
caption = "" 
+++

Environment used to developed world model<br\>
&nbsp;  &nbsp;  &nbsp;  - OS: Ubuntu 16.04 server<br\>
&nbsp;  &nbsp;  &nbsp;  - Python version : 3.5.4<br\>


1. install openai gym<br\>
&nbsp;  &nbsp;  &nbsp;  - pip install gym==0.9.4<br\>
2. install cma<br\>
&nbsp;  &nbsp;  &nbsp;  - pip install cma==2.2.0<br\>
3. install mpi4py<br\>
&nbsp;  &nbsp;  &nbsp;  - conda install -c anaconda mpi4py<br\>
&nbsp;  &nbsp;  &nbsp;  - installed mpi4py-2.0.0<br\>
4. install gym-pull<br\>
&nbsp;  &nbsp;  &nbsp;  - pip install gym-pull<br\>
5. To install dependencies<br\>
&nbsp;  &nbsp;  &nbsp;  - apt-get install -y python-numpy cmake zlib1g-dev libjpeg-dev libboost-all-dev gcc libsdl2-dev wget unzip git<br\>
6. install pybox2d<br\>
&nbsp;  &nbsp;  &nbsp;  - https://github.com/pybox2d/pybox2d/blob/master/INSTALL.md<br\>
&nbsp;  &nbsp;  &nbsp;  - conda install -c https://conda.anaconda.org/kne pybox2d<br\>
7. install spicy<br\>
&nbsp;  &nbsp;  &nbsp;  - pip install spicy<br\>
8. Install pillow<br\>
&nbsp;  &nbsp;  &nbsp;  - pip install pillow<br\>
9. Download worldmodel from github<br\>
&nbsp;  &nbsp;  &nbsp;  - https://github.com/hardmaru/WorldModelsExperiments <br\>
10. Execute car racing<br\>
&nbsp;  &nbsp;  &nbsp;  - Navigate to ../WorldModelsExperiments-master/carracing<br\>
&nbsp;  &nbsp;  &nbsp;  - python model.py render log/carracing.cma.16.64.best.json<br\>
&nbsp;  &nbsp;  &nbsp;  - model size 867<br\>
&nbsp;  &nbsp;  &nbsp;  - loading file log/carracing.cma.16.64.best.json<br\>
&nbsp;  &nbsp;  &nbsp;  - Track generation: 1048..1314 -> 266-tiles track<br\>
&nbsp;  &nbsp;  &nbsp;  - total reward 923.0999999999923 timesteps 768<br\>
&nbsp;  &nbsp;  &nbsp;  - terminal reward [923.0999999999923] average steps taken 769.0<br\>
&nbsp;  &nbsp;  &nbsp;  - Navigate to ../WorldModelsExperiments-master/doomrnn<br\>
10. Execute doomrnn racing<br\>
&nbsp;  &nbsp;  &nbsp;  - python model.py doomreal render log/doomrnn.cma.16.64.best.json<br\>
&nbsp;  &nbsp;  &nbsp;  - ImportError: No module named 'doom_py'<br\>
&nbsp;  &nbsp;  &nbsp;  - download gymdoom from https://github.com/ppaquette/gym-doom<br\>
&nbsp;  &nbsp;  &nbsp;  - nativate ../../gym-doom-master<br\>
&nbsp;  &nbsp;  &nbsp;  - execute python setup.py build<br\>
&nbsp;  &nbsp;  &nbsp;  - pip install ppaquette-gym-doom<br\>
11. ZDoom dependencies<br\>
&nbsp;  &nbsp;  &nbsp;  - sudo apt-get install build-essential zlib1g-dev libsdl2-dev libjpeg-dev nasm tar libbz2-dev libgtk2.0-dev cmake git libfluidsynth-dev libgme-dev libopenal-dev timidity libwildmidi-dev unzip<br\>
12. Boost libraries<br\>
&nbsp;  &nbsp;  &nbsp;  - sudo apt-get install libboost-all-dev<br\>
13. Python 3 dependencies<br\>
&nbsp;  &nbsp;  &nbsp;  - sudo apt-get install python3-dev python3-pip<br\>
14. pip install git+https://github.com/mwydmuch/ViZDoom<br\>
&nbsp;  &nbsp;  &nbsp;  - Error<br\> 
&nbsp;  &nbsp;  &nbsp;  - subprocess.CalledProcessError: Command '['make', '-j', '35']' returned non-zero exit status 2<br\>
&nbsp;  &nbsp;  &nbsp;  - source deactivate worldmodel<br\>
&nbsp;  &nbsp;  &nbsp;  - conda remove harfbuzz<br\>
&nbsp;  &nbsp;  &nbsp;  - Source activate worldmodel<br\>
&nbsp;  &nbsp;  &nbsp;  - pip install git+https://github.com/mwydmuch/ViZDoom<br\>
15. pip install matplotlib<br\>
16. Navigate to ../WorldModelsExperiments-master/doomrnn<br\>
17. python model.py doomreal render log/doomrnn.cma.16.64.best.json<br\>
&nbsp;  &nbsp;  &nbsp;  - reward 399.0 timesteps 398<br\>
&nbsp;  &nbsp;  &nbsp;  - terminal reward [399.0] average steps taken 399.0

