# Troubleshooting — JetRover Tank ROS2

## ROS2 commands not found
```bash
source /opt/ros/humble/setup.bash
source ~/jetrover_ws/install/setup.bash
```

## No topics visible
```bash
ros2 node list
ros2 topic list
```

## Camera issues
```bash
ros2 topic list | grep -i image
rqt_image_view
```

## Robot not moving
- Confirm correct velocity topic exists (commonly `/cmd_vel`)
- Test stop then low-speed forward
```bash
ros2 topic pub --once <cmd_vel_topic> geometry_msgs/msg/Twist "{linear: {x: 0.0}, angular: {z: 0.0}}"
ros2 topic pub --once <cmd_vel_topic> geometry_msgs/msg/Twist "{linear: {x: 0.05}, angular: {z: 0.0}}"
```

## Note
All commands are run on the robot via NoMachine.
