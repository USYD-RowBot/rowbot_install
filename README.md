# rowbot_install

This assumes you have ros-kinetic installed and already have a catkin workspace created
This will require, hector-gazbebo-plugins.
Install using 'sudo apt-get install ros-kinetic-hector-gazebo-plugins'
To install: Move simulator.rosinstall to your src folder and rename to .rosinstall. Then run in terminal 'rosws update'

Make your workspace using catkin_make. Run '/devel/setup.bash'

To launch. Run 'roslaunch rowbot_sim_bringup bringup.launch'.



Commands
```
cd ~
mkdir-p catkin_ws/src

sudo apt-get install ros-kinetic-hector-gazebo-plugins
sudo apt-get install ros-kinetic-pointcloud-to-laserscan
sudo apt-get install ros-kinetic-navigation
sudo apt-get install ros-kientic-teb-local-planner
gedit .rosinstall
```
Copy contents of simulator.install in here
```
rosws update
cd ..
catkin_make
echo "source ~/catkin_ws/devel/setup.bash" >> ~/.bashrc

roslaunch rowbot_sim_bringup bringup.launch
```

# Alternative Installation

You can use wstool to install

```bash
# install dependencies
sudo apt-get install ros-kinetic-hector-gazebo-plugins ros-kinetic-pointcloud-to-laserscan ros-kinetic-navigation ros-kientic-teb-local-planner
mkdir -p ~/catkin_ws/src && cd ~/catkin_ws/src
git clone https://github.com/USYD-RowBot/rowbot_install.git
wstool init . rowbot_install/simulator.rosinstall
catkin_make
```

