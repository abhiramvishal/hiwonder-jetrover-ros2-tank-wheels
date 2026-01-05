# 01 — Environment Setup (JetRover Tank + ROS2)

This guide assumes ROS2 is installed on the JetRover Tank and you access it using NoMachine.

## Assumptions
- JetRover Tank and laptop are on the same Wi-Fi
- You run ROS2 on the robot via NoMachine terminal
- ROS2 Humble is installed on the robot

## Create a ROS2 workspace
```bash
mkdir -p ~/jetrover_ws/src
cd ~/jetrover_ws
colcon build
source install/setup.bash
```

## Auto-source workspace
```bash
echo "source ~/jetrover_ws/install/setup.bash" >> ~/.bashrc
source ~/.bashrc
```

## Verify ROS2
```bash
ros2 --version
ros2 topic list
```

Next → `docs/02-ros2-basics.md`
