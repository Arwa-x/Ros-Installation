# Ros Installation on ubuntu

## 1- Download an Ubuntu Image

1.1 Download an Ubuntu image

Download link: https://ubuntu.com/download/desktop

and save its location to add it later to the VirtualBox

The version I download is Ubuntu 20.04.4 Desktop (64-bit)

## 2- Download and install VirtualBox

2.1 Download and install the latest version of VirtualBox 

Download link: https://www.virtualbox.org/wiki/Downloads

The version I download is 6.1.34

2.2 After the installation is completed, run VirtualBox then create a new virtual machine by Clicking "New"

2.3 Then type any name and select the type you want then click "Next"

2.4 As you move to the next screen, you can select how much memory is to be allocated from your main computer to the virtual machine 

2.5 After that, select how much of your hard disk your VM will use then click "Create"

2.6 Select the type of file you will use for your Virtual hard disk

2.6 Choose whether the hard disk is dynamically allocated or has a fixed size

2.7 Finally set the size of the of memory your VM can access, then click "Create" to initialize the machine

## 3- Install Ubuntu Image

3.1 Click "Start" to launch the virtual machine

3.2 Select the start-up disk, click the file icon to open the Optical disc selector and click Add to find your .iso file that you download before, then click "Start"

3.3 AFter Ubuntu desktop appears click "Insatall Ubuntu"

3.4 Follow the steps and if the default is good click "Continue"

3.5 Enter your preferred name, username and password then click "Continue"

3.6 The installation will start and after it is finished click Restart now then press "Enter"

3.7 Finally enter the password you have chosen and press "Enter", now your Ubuntu Desktop OS is ready

## 4- Install ROS in ubuntu

4.1 From ubuntu go to firefox browser then search for Ros installation and choose the version that is recommended to the ubuntu version that you have installed before

The version of ROS I used for Ubuntu 20.04.4 is ROS Noetic

Link: http://wiki.ros.org/Installation/Ubuntu website

4.3 On the search bar of ubuntu type Terminal and open it

4.4 copy these instructions one by one and paste it into the terminal to install it

### Setup your sources.list
```
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
```
### Set up your keys
```
sudo apt install curl # if you haven't already installed curl
curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
```
### Installation
First, make sure your Debian package index is up-to-date:
```
sudo apt update
```
Now pick how much of ROS you would like to install:
#### Desktop-Full Install: (Recommended) : Everything in Desktop plus 2D/3D simulators and 2D/3D perception packages
```
sudo apt install ros-noetic-desktop-full
```
#### Desktop Install: Everything in ROS-Base plus tools like rqt and rviz
```
sudo apt install ros-noetic-desktop
```
#### ROS-Base: (Bare Bones) ROS packaging, build, and communication libraries. No GUI tools
```
sudo apt install ros-noetic-ros-base
```
### Environment setup
```
source /opt/ros/noetic/setup.bash
```
### Dependencies for building packages
```
sudo apt install python3-rosdep python3-rosinstall python3-rosinstall-generator python3-wstool build-essential
```
### Initialize rosdep
```
sudo apt install python3-rosdep
```
```
sudo rosdep init
rosdep update
```

4.5 After installation has finished, test it by using this command to ensure that it has been installed successfully
```
roscore
```
4.6 Finally, press Ctrl+C in the terminal to stop roscore
