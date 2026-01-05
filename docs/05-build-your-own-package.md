# 05 — Build Your Own ROS2 Package (Tank Movement)

Create a ROS2 Python package to publish velocity commands for the JetRover Tank.

## Create package
```bash
cd ~/jetrover_ws/src
ros2 pkg create --build-type ament_python jetrover_tank_motion --dependencies rclpy geometry_msgs
```

## Goal
Implement simple scripts:
- `move_forward.py`
- `rotate_left.py`
- `rotate_right.py`
- `stop.py`

Each script publishes a `Twist` message to `<cmd_vel_topic>`.

## Build workspace
```bash
cd ~/jetrover_ws
colcon build
source install/setup.bash
```

## Run (example)
```bash
# ros2 run jetrover_tank_motion move_forward
# ros2 run jetrover_tank_motion stop
```

Next → `docs/troubleshooting.md`
