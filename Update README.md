# Steps to Install ROS2 On Jetson Nano 
### "task two"
#### The Jetson Nano is the latest embedded board of the NVIDIA Jetson family. 
Designed for autonomous machines, it is a tiny, low power and affordable platform with a high level of computing power 
allowing to perform real time computer vision and mobile-level deep learning operations at the edge.

<div>
  <img src="https://user-images.githubusercontent.com/109974986/183987598-5ef671cc-38c7-4b57-bcd7-d64bcaff981a.jpg" width="300">
  </div>
  
#### - The first step is to install XUbuntu 20 from following link:
https://forums.developer.nvidia.com/t/xubuntu-20-04-focal-fossa-l4t-r32-3-1-custom-image-for-the-jetson-nano/121768
#### Open XUbuntu and write the following commands to extract Xubutun image:
```
tar -xvjf Xubuntu-20.04-l4t-r32.3.1.tar.tbz2
```
## Download balena
#### https://www.balena.io/etcher/
#### open the program and select the image, then select the device port name. then insert the SD card in Jetson Nano.
## ROS 2 install
#### open the terminal to write the ROS 2 installation commands.
### - Set locale
```
locale  # check for UTF-8
sudo apt update && sudo apt install locales
sudo locale-gen en_US en_US.UTF-8
sudo update-locale LC_ALL=en_US.UTF-8 LANG=en_US.UTF-8
export LANG=en_US.UTF-8
locale
```
### - Setup Sources
```
apt-cache policy | grep universe or

sudo apt install software-properties-common

sudo add-apt-repository universe

sudo apt update && sudo apt install curl gnupg2 lsb-release

sudo curl -sSL https://raw.githubusercontent.com/ros/rosdistro/master/ros.key -o /usr/share/keyrings/ros-archive-keyring.gpg

echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/ros-archive-keyring.gpg] http://packages.ros.org/ros2/ubuntu $(source /etc/os-release && echo $UBUNTU_CODENAME) main" | sudo tee /etc/apt/sources.list.d/ros2.list > /dev/null
```
### Install ROS 2 packages
```
sudo apt update
sudo apt upgrade
sudo apt install ros-foxy-desktop
sudo apt install ros-foxy-ros-base
```
## Environment setup
```
echo "source /opt/ros/foxy/setup.bash" >> ~/.bashrc
source ~/.bashrc
```
