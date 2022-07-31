# Steps-to-install-ROS-on-ubuntu-20.4
### first task
#### The first step is to download the VirtualBox software
#### The next step is to install Linux (Ubuntu) into the virtualBox 

<div>
<img src="https://user-images.githubusercontent.com/109974986/182042367-c7f19854-bd62-43d8-a8f9-f0f3b30fb2d8.jpg" width="300">
  </div>
  
#### After that, enter the Ubuntu system, open the Terminal, and write the code for the rose that is compatible with the Ubuntu 20.4 version.

<div>
<img src="https://user-images.githubusercontent.com/109974986/182042603-03c37d0d-c223-4d71-afb3-6b6e6846ab0d.jpg" width="300">
      </div>
      
## Ubuntu install of ROS Noetic:
### code:
```
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
```
```
sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE88688172B4F42ED6FBAB17C654
```
```
sudo apt update
```
###### Desktop-Full Install: (Recommended) : Everything in Desktop plus 2D/3D simulators and 2D/3D perception packages
```
sudo apt install ros-noetic-desktop-full
```
```
source /opt/ros/noetic/setup.bash
```
```
roscore
```
<div>
<img src="https://user-images.githubusercontent.com/109974986/182045628-f142cab4-897b-4e67-8697-ccc1cc2d1963.jpg" width="400">
  </div>
  
