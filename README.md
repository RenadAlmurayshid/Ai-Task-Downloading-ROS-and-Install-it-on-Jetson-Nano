# Ai-Task-Downloading-ROS-and-Install-it-on-Jetson-Nano
This is a repository for the first task in smart methods which is ros installation 

1)	Download the virtual box 
2)	Download Ubuntu 18.04.5
3)	Download ROS (Melodic type ) 
4)	Download and run RVIZ 


Link for the virtual box installation :
 https://www.virtualbox.org/wiki/Downloads
Link for ubuntu 18.04.5  :  https://www.virtualbox.org/wiki/Downloads


For the ROS download I have chosen the melodic the instruction are linked  here : 
http://wiki.ros.org/ROS/Installation

for the ubuntu platform I have chosen LINUX 


steps for melodic arm were taken from this link : 

https://github.com/smart-methods/arduino_robot_arm

extra notes to take in consideration after writing sudo nano ~/.bashrc (on the last lines) :

change the system name to your liking 

source /home/renadalmurayshid/catkin_ws/devel/setup.bash

after that press the following buttons :
1)	CTRL + O 
2)	ENTER 
3)	CTRL + X 

Go to the source with this command : 
source ~/.bashrc

lastly launch the ROS  with this command : 
roslaunch robot_arm_pkg check_motors.launch


***********************************************************************************
Task 2 installation of ROS on jetson nano 
This command lists was from :
https://github.com/AnbuKumar-maker/ROS-Installation-on-Jetson-Nano/tree/m

1-	Fist thing you need to do is to install the package with this command :

sudo sh -c 'echo "deb  http://packages.ros.org/ros/ubuntu  $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list


2-	You need to put the package key 

sudo apt-key adv --keyserver 'hkp://keyserver.ubuntu.com:80' --recv-key C1CF6E31E6BADE8868B172B4F42ED6FBAB17C654


3-	You must update this package from this command 

sudo apt update

4-	Use the command to install the melodic ros  : 

sudo apt install ros-melodic-desktop


5-	Ros initiation : 

sudo rosdep init

6-	Update your Ros :
         rosdep update
7-	Get to the source of melodic ROS 
echo "source /opt/ros/melodic/setup.bash" >> ~/.bashr

8-	Confirm your source : 

source ~/.bashrc

9-	Make sure that your work is done by using this command Melodic shall be the output 
rosversion -d

