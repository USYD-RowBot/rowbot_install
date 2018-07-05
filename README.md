# rowbot_install

This assumes you have ros-kinetic installed and already have a catkin workspace created
This will require, hector-gazbebo-plugins.
Install using 'sudo apt-get install ros-kinetic-hector-gazebo-plugins'
To install: Move simulator.rosinstall to your src folder and rename to .rosinstall. Then run in terminal 'rosws update'

Make your workspace using catkin_make. Run '/devel/setup.bash'

To launch. Run 'roslaunch rowbot_sim_bringup bringup.launch'.
