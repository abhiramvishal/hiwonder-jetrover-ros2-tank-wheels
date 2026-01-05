# 03 — Camera Bring-Up and Viewing

This section explains how to bring up the JetRover Tank camera and view the live stream.

## Start camera (example)
```bash
# ros2 launch peripherals depth_camera.launch.py
```

## Find camera topic
```bash
ros2 topic list
```

Common example:
`/depth_cam/rgb/image_raw`

## View stream
```bash
rqt_image_view
```

## Check message type
```bash
ros2 topic type <camera_topic_name>
```

Expected:
`sensor_msgs/msg/Image`

Next → `docs/04-movement-tank.md`
