# 04 — Tank Movement (Tracked Drive)

Tracked robots generally support:
- Forward / backward via `linear.x`
- Rotation (turn-in-place) via `angular.z`

All commands are executed **on the robot**.

---

## 1) Identify the velocity topic

```bash
ros2 topic list
```

Look for a topic like:
- `/cmd_vel`

Confirm type:
```bash
ros2 topic type <cmd_vel_topic>
```

Expected:
- `geometry_msgs/msg/Twist`

---

## 2) Safety first (stop)

```bash
ros2 topic pub --once <cmd_vel_topic> geometry_msgs/msg/Twist "{linear: {x: 0.0}, angular: {z: 0.0}}"
```

---

## 3) Basic movement commands

### Forward
```bash
ros2 topic pub --once <cmd_vel_topic> geometry_msgs/msg/Twist "{linear: {x: 0.10}, angular: {z: 0.0}}"
```

### Backward
```bash
ros2 topic pub --once <cmd_vel_topic> geometry_msgs/msg/Twist "{linear: {x: -0.10}, angular: {z: 0.0}}"
```

### Rotate left (counter-clockwise)
```bash
ros2 topic pub --once <cmd_vel_topic> geometry_msgs/msg/Twist "{linear: {x: 0.0}, angular: {z: 0.6}}"
```

### Rotate right (clockwise)
```bash
ros2 topic pub --once <cmd_vel_topic> geometry_msgs/msg/Twist "{linear: {x: 0.0}, angular: {z: -0.6}}"
```

### Stop
```bash
ros2 topic pub --once <cmd_vel_topic> geometry_msgs/msg/Twist "{linear: {x: 0.0}, angular: {z: 0.0}}"
```

---

## 4) Pivot turns (slow curve turns)

### Gentle left curve
```bash
ros2 topic pub --once <cmd_vel_topic> geometry_msgs/msg/Twist "{linear: {x: 0.08}, angular: {z: 0.25}}"
```

### Gentle right curve
```bash
ros2 topic pub --once <cmd_vel_topic> geometry_msgs/msg/Twist "{linear: {x: 0.08}, angular: {z: -0.25}}"
```

---

## Notes
- Tracks can grip hard; start with low speeds: **0.05–0.10**
- If turning is too aggressive, reduce `angular.z`
- No sideways movement is expected for tracked drive

Next → `docs/05-build-your-own-package.md`
