
# Ros 2 Installation on Jetson Nano

## 1- Download XUbuntu
1.1	Download the custom image for Jeston Nano version 20.04

Download Link: https://github.com/Discombobulated88/Xubuntu-20.04-L4T-32.3.1/releases/download/v1.0/Xubuntu-20.04-l4t-r32.3.1.tar.tbz2

1.2 Unzip/Extract it till it gives you the .img file

## 2- Download Balena
2.1 Download, install, and launch Etcher to write the XUbuntu Image to your SD card

It’s important to have a card that’s fast and large enough, the minimum recommended is a 32 GB card

2.2 Insert your SD card if not already inserted

2.3 Click “Select drive” and choose your SD card

2.4 Click “Select image” and choose the XUbuntu .img file you downloaded earlier

2.5 Click “Flash!” it will take time to write and validate the image

2.6 After Etcher finishes, Windows prompts you with a dialog of formatting the disk just click Cancel and remove the SD card

2.7 Insert the SD card into the slot on the underside of the Jetson Nano

2.8 Connect your keyboard/mouse/monitor and power

## 3- Install Ros 2
3.1 After the XUbuntu image loaded, open firefox and search for Ros 2 installation

Link: https://docs.ros.org/en/foxy/Installation/Ubuntu-Install-Debians.html

3.2	Coby these instructions into the terminal to install it 
### Set locale
Make sure you have a locale which supports UTF-8
```
locale  # check for UTF-8

sudo apt update && sudo apt install locales
sudo locale-gen en_US en_US.UTF-8
sudo update-locale LC_ALL=en_US.UTF-8 LANG=en_US.UTF-8
export LANG=en_US.UTF-8

locale  # verify settings
```

### Setup sources
You will need to add the ROS 2 apt repositories to your system. First, make sure that the Ubuntu Universe repository is enabled by checking the output of this command
```
apt-cache policy | grep universe
```
This should output a line like the one below:
```
500 http://us.archive.ubuntu.com/ubuntu focal/universe amd64 Packages
    release v=20.04,o=Ubuntu,a=focal,n=focal,l=Ubuntu,c=universe,b=amd64
```
If you don’t see an output line like the one above, then enable the Universe repository with these instructions
```
sudo apt install software-properties-common
sudo add-apt-repository universe
```
Now add the ROS 2 apt repository to your system
```
sudo apt update && sudo apt install curl gnupg2 lsb-release
sudo curl -sSL https://raw.githubusercontent.com/ros/rosdistro/master/ros.key  -o /usr/share/keyrings/ros-archive-keyring.gpg
```
Then add the repository to your sources list
```
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/ros-archive-keyring.gpg] http://packages.ros.org/ros2/ubuntu $(source /etc/os-release && echo $UBUNTU_CODENAME) main" | sudo tee /etc/apt/sources.list.d/ros2.list > /dev/null
```
### Install ROS 2 packages
Update your apt repository caches after setting up the repositories
```
sudo apt update
```
It is always recommended that you ensure your system is up to date before installing new packages
```
sudo apt upgrade
```
Desktop Install (Recommended): ROS, RViz, demos, tutorials
```
sudo apt install ros-foxy-desktop
```
ROS-Base Install (Bare Bones): Communication libraries, message packages, command line tools. No GUI tools
```
sudo apt install ros-foxy-ros-base
```
### Environment setup
Set up your environment by sourcing the following file
```
source /opt/ros/foxy/setup.bash
```
### Try some examples
In one terminal, source the setup file and then run a C++ talker:
```
ros2 run demo_nodes_cpp talker
```
In another terminal source the setup file and then run a Python listener:
```
ros2 run demo_nodes_py listener
```
### Testing
After installation has finished test it by this command to ensure that it has been installed successfully
```
ros2 topic list
```
