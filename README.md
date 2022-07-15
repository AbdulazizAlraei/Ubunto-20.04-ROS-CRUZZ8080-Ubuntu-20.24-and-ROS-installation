# Ubunto-20.04-ROS-CRUZZ8080-Ubuntu-20.24-and-ROS-installation
The installation steps of Ubuntu and ROS

## First Ubuntu 20.04.4 Installation steps:

1-Download and install VirtualBox.

2-Download Ubuntu 20.04.4 LTS Desktop Image from this URL: https://releases.ubuntu.com/20.04/ubuntu-20.04.4-desktop-amd64.iso

3-After installing VirtualBox, click New to make a new virtual machine.

4-Type **Ubuntu** in the field `Name`.

5-Set the `type` to `Linux`, and `version` to `Ubuntu (64-bit)` then click Next.

6-Set the Memory size to the end of the green bar and click Next.

7-Click Next and then click Create.

8-After creating the virtual machine we should connect Ubuntu image that we downloaded in step number 1, we do that by double clicking on the virtual machine.

9-After launching the virtual machine, click browse and choose the Ubuntu image then click Start.

10-Click  `Install Ubuntu` then continue and wait until the installation is finished.


## Second ROS Noetic Installation steps:
1- Enter the command terminal

2-Configure your Ubuntu repositories (`universe`,`multiverse`,`restricted`) by using these commands:

sudo add-apt-repository universe

```
then
```

sudo add-apt-repository multiverse
```

then
```

sudo add-apt-repository restricted
```

then
```

sudo apt-get update
```

3-Setup your computer to accept software from packages.ros.org.

```
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'

```


4-Set up your keys using these commands:

```
sudo apt install curl 
```

then
```
curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -
```

then
```
sudo apt update
```

5-Install Desktop full version:

```
sudo apt install ros-noetic-desktop-full
```

6-Setup the environment using these commands:

```
source /opt/ros/noetic/setup.bash
```

```
echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc
```

```
source ~/.bashrc
```

```
echo "source /opt/ros/noetic/setup.zsh" >> ~/.zshrc
```

```
source ~/.zshrc
```


7-Install the dependencies for building packages:

```
sudo apt install python3-rosdep python3-rosinstall python3-rosinstall-generator python3-wstool build-essential
```

```
sudo apt install python3-rosdep
```

8-Initialize rosdep:

```
sudo rosdep init
```

```
rosdep update
```




**Reference**: http://wiki.ros.org/noetic/Installation/Ubuntu



