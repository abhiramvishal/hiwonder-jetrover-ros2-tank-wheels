# Hiwonder JetRover Tank (Tracked Wheels) — ROS2 On-Robot Guide

This repository is a **course-style ROS2 guide** for working with the **Hiwonder JetRover Tank** (tracked wheels).

All ROS2 code is executed **directly on the robot**, while the laptop connects via **NoMachine** over the same Wi-Fi network.

---

## What’s different with tank tracks?
Tracked wheels are excellent for stability and rough surfaces. Movement is typically:
- Forward / backward (x-axis)
- Rotate in place (z-axis)

Unlike mecanum wheels, **sideways (strafe) motion is not supported**.

---

## What this repository covers
- ROS2 workspace setup on the JetRover Tank
- Camera bring-up and topic inspection
- Tank movement control (forward, rotate, stop, pivots)
- Creating custom ROS2 Python packages for motion control
- Foundation for perception-driven robotics projects

---

## Setup assumptions
- Robot and laptop are connected to the **same Wi-Fi**
- You connect to the robot using **NoMachine**
- ROS2 runs **on the robot**, not on the laptop

---

## Quick start (run on the robot)

```bash
mkdir -p ~/jetrover_ws/src
cd ~/jetrover_ws
colcon build
source install/setup.bash
```

Check ROS2:
```bash
ros2 topic list
```

---

## Learning path
Follow these files in order:

1. `docs/01-setup.md`
2. `docs/02-ros2-basics.md`
3. `docs/03-camera.md`
4. `docs/04-movement-tank.md`
5. `docs/05-build-your-own-package.md`
6. `docs/troubleshooting.md`

---

## License
© Macquarie University — Academic Coursework  
Intended for educational and demonstration purposes.
