# roboclaw_node
Control based on Roboclaw Controller in ROS environment  
Improved the following repositories  
https://github.com/sonyccd/roboclaw_ros  
Explanation article(Japanese)
https://qiita.com/fujikawabata/items/a716694accc3cc52784e

# Improvement
From Speed to Accelerate and Speed  
Add script to publish /cmd_vel  
Add script to subscribe /odom  

# Requirement
Ubuntu mate 16.04  
ROS kinetic

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
If you want to publish the speed command
```
$ rosrun roboclaw_node talker-twist.py
```
If you want to subscribe to velocity, orientation and pose
```
$ rosrun roboclaw_node listen-odom.py
```
If yout want to teoperate the robot
```
$ rosrun roboclaw_node teleop_key.py
```
