# roboclaw_node
Control based on Roboclaw Controller in ROS environment  
Improved the following repositories  
https://github.com/sonyccd/roboclaw_ros

# Improvement
From Speed to Accelerate and Speed  
Add script to publish /cmd_vel  
Add script to subscribe /odom  

# Requirement
Ubuntu mate 16.04  
ROS kinetic  
Roboclaw controller version is 4.1.33

# How to use
Clone this repo
```
$ ~/your workspace/src/
$ sudo git clone https://github.com/bata-kawa3/roboclaw_node.git
$ cd ..
$ catkin_make
```
Start the master and run the script to calculate odometry
```
$ roslaunch roboclaw_node roboclaw.launch
```
When issuing a speed command
```
$ rosrun roboclaw_node talker-twist.py
```
When reading velocity, orientation and pose from Geometry_msg
```
$ rosrun roboclaw_node listen-odom.py
```
