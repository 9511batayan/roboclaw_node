# roboclaw_node
Control based on Roboclaw Controller in ROS environment

# Requirement
Ubuntu mate 16.04  
ROS kinetic  
Roboclaw controller version is 4.1.33

# How to use
Start the master and run the script to calculate odometry
```
roslaunch roboclaw_node roboclaw.launch
```
When issuing a speed command
```
rosrun roboclaw_node talker-twist.py
```
When reading Geometry_msg such as odometry
```
rosrun roboclaw_node listen-odom.py
```
