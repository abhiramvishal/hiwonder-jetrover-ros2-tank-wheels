# 02 — ROS2 Basics (Minimum You Need)

ROS2 is the communication layer between sensors and motion control on the robot.

## Core concepts
- Node: running program
- Topic: data channel
- Publisher: sends messages
- Subscriber: receives messages

## Commands
```bash
ros2 node list
ros2 topic list
ros2 topic type <topic_name>
ros2 topic info <topic_name>
ros2 topic echo <topic_name>
```

## JetRover Tank essentials
You mainly need:
- Camera topic
- Velocity topic (commonly `/cmd_vel`)

Next → `docs/03-camera.md`
