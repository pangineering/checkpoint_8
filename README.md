# The rb1_ros2_description package

This package contains a ROS2 robot model description for Robotnik's RB-1 mobile base.   

## Installation Instructions
Before installing this package, please ensure you have the following prerequisites installed:
- ROS 2 (Foxy or later)
- Gazebo (version compatible with ROS 2 distribution)
- ROS 2 Control (`ros2_control` and `ros2_controllers` packages)

Once you have installed the prerequisites, you can install the rb1_ros2_description package by cloning the repository into your ROS 2 workspace and building it using colcon:
```bash
cd <your_ros2_workspace>/src
git clone <repository_url>
cd ..
colcon build
```

---
## Disclaimer:  
This package only modifies/adapts files from these repositories/packages:  
- [RobotnikAutomation/rb1_base_sim](https://github.com/RobotnikAutomation/rb1_base_sim) licensed under the BSD 2-Clause "Simplified" License
- [RobotnikAutomation/rb1_base_common/rb1_base_description](https://github.com/RobotnikAutomation/rb1_base_common/tree/melodic-devel/rb1_base_description), licensed under the BSD License
- [RobotnikAutomation/robotnik_sensors],(https://github.com/RobotnikAutomation/robotnik_sensors) licensed under the BSD License
