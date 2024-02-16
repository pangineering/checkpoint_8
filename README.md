# The rb1_ros2_description package

This package contains a ROS2 robot model description for Robotnik's RB-1 mobile base.   

## Installation Instructions
Before installing this package, please ensure you have the following prerequisites installed:
- ROS 2 (Foxy or later)
- Gazebo (version compatible with ROS 2 distribution)
- ROS 2 Control (`ros2_control` and `ros2_controllers` packages)

Once you have installed the prerequisites, you can install the rb1_ros2_description package by cloning the repository into your ROS 2 workspace and building it using colcon:
```bash
cd ros2_ws/src
git clone [<repository_url>](https://github.com/pangineering/checkpoint_8.git)
cd ..
colcon build
```

## Getting Started

To run the simulation with the RB1 robot model, follow these steps:

1. Launch the Gazebo simulation with the RB1 robot model:
```bash
ros2 launch rb1_gazebo rb1_simulation.launch.py
```

## Controllers
```bash
ros2 control list_hardware_interfaces
```
```bash
ros2 control list_controllers
```

## Move the robot
1. Using the teleop
```bash
ros2 run teleop_twist_keyboard teleop_twist_keyboard --ros-args --remap cmd_vel:=/rb1_base_controller/cmd_vel_unstamped
```   
2. Using the command line
```bash
ros2 topic pub --rate 10 /rb1_base_controller/cmd_vel_unstamped geometry_msgs/msg/Twist "{linear: {x: 0.0, y: 0, z: 0.0}, angular: {x: 0.0,y: 0.0, z: 0.2}}"
```

## Moving the Robot's Lifting Unit
---
## Disclaimer:  
This package only modifies/adapts files from these repositories/packages:  
- [RobotnikAutomation/rb1_base_sim](https://github.com/RobotnikAutomation/rb1_base_sim) licensed under the BSD 2-Clause "Simplified" License
- [RobotnikAutomation/rb1_base_common/rb1_base_description](https://github.com/RobotnikAutomation/rb1_base_common/tree/melodic-devel/rb1_base_description), licensed under the BSD License
- [RobotnikAutomation/robotnik_sensors],(https://github.com/RobotnikAutomation/robotnik_sensors) licensed under the BSD License
