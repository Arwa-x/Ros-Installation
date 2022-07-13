# Ros Installation in ubuntu

## 1- Download an Ubuntu Image

1.1 Download an Ubuntu image from https://ubuntu.com/download/desktop

and save its location to add it later to the VirtualBox

The version I used is Ubuntu 20.04.4 Desktop (64-bit)


## 2- Download and install VirtualBox

2.1 Download and install the latest version of VirtualBox from https://www.virtualbox.org/wiki/Downloads

The version I download is 6.1.34

2.2 After the installation is completed, run VirtualBox then create a new virtual machine by Clicking (New) 

2.3 Then type any name and select the type you want then click Next 

2.4 As you move to the next screen, you can select how much memory is to be allocated from your main computer to the virtual machine 

2.5 After that, select how much of your hard disk your VM will use then click create

2.6 Then select the type of file you will use for your Virtual hard disk

2.6 Choose whether the hard disk is dynamically allocated or has a fixed size

2.7 Finally set the size of the of memory your VM can access, then click Create to initialize the machine

## 3- Install Ubuntu Image

3.1 Click Start to launch the virtual machine

3.2 Select the start-up disk, click the file icon to open the Optical disc selector and click Add to find your .iso file that you download before, then click Start

3.3 AFter Ubuntu desktop appears click insatall Ubuntu

3.4 Follow the steps and if the default is good click Continue

3.5 Enter your preferred name, username and password then click Continue

3.6 The installation will start and after it is finished click Restart now then press Enter

3.7 Finally enter the password you have chosen and press Enter and your Ubuntu Desktop OS is ready

## 4- Install ROS in ubuntu

4.1 From ubuntu enter Firefox browser and search http://wiki.ros.org/Installation/Ubuntu website

4.2 Search and choose ROS version that is recommended to the ubuntu version that you have installed before

The version of ROS I used for Ubuntu 20.04.4 is ROS Noetic

4.3 On the search bar of ubuntu type Terminal and open it

4.4 Follow the steps of instalation in the website

4.5 On the terminal paste all instructions you copied from the website one by one

4.6 After installation is completed type roscore in the terminal to ensure that it has been installed successfully then press Ctrl+C in the terminal to stop roscore

