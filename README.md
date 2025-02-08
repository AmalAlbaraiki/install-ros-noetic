# install-ros-noetic
Introduction:
ROS Noetic is the Long-Term Support (LTS) release of the Robot Operating
System (ROS). It is designed to work with Ubuntu 20.04 (Focal Fossa). In this report, we will go over all the steps required to install ROS Noetic on an Ubuntu system.

Steps:
1. Prepare the Environment
Before starting with the installation of ROS Noetic, make sure you are using Ubuntu 20.04 or later, as this is the supported version for ROS Noetic. If you are using a different version of Ubuntu, you should upgrade to the supported version.

2. Update Your System
Start by updating the packages on your current system:


sudo apt update

sudo apt upgrade


3. Add the ROS Repository
   
Add the ROS repository to your system:


sudo sh -c 'echo "deb [arch=amd64] http://packages.ros.org/ros/ubuntu focal main" > /etc/apt/sources.list.d/ros-latest.list'

4. Add the GPG Key
   
You need to add the GPG key for the ROS repositories:


curl -s https://raw.githubusercontent.com/ros/rosdistro/master/ros.asc | sudo apt-key add -

5. Update the Package List
   
Once the repository and key are added, update the package list:


sudo apt update


6. Install ROS Noetic
   
Now, you can install ROS Noetic using the following command:

sudo apt install ros-noetic-desktop-full

This might take some time depending on your internet speed and system performance.

7. Set Up Your Environment
   
After installation, you need to set up the ROS environment. To ensure that ROS loads automatically in each new terminal session, add the following line to your .bashrc file:



echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc

source ~/.bashrc

8. Install Build Tools (Optional)
   
If you need build tools like catkin, you can install them by running:


sudo apt install python3-catkin-tools

9. Verify the Installation
    
Once everything is installed, verify that ROS Noetic is installed correctly by running:


roscore

If roscore runs successfully without errors, it means ROS has been installed correctly.

10. Create a Workspace (Optional)

If you plan to work on projects using ROS Noetic, you can create a new workspace by running:


تحرير
mkdir -p ~/catkin_ws/src
cd ~/catkin_ws/
catkin_make
source devel/setup.bash
Now you can start working on your projects inside this workspace.



Conclusion:
Once you’ve completed all the steps, ROS Noetic will be installed correctly on your system. You can now begin using it to develop robotics applications.

