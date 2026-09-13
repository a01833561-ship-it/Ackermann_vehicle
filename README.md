# Ackermann Vehicle Simulation

ROS 2 and Gazebo simulation of the Ackermann vehicle, including the vehicle description, sensors, Gazebo simulation, and ROS 2 control interfaces.

## Requirements

The simulation requires:

- Ubuntu
- ROS 2
- Gazebo
- `colcon`
- `ros_gz_sim`
- `xacro`

Make sure ROS 2 is installed and sourced before building.

---

## 1. Workspace Structure

The workspace should have the following structure:

```text
sm26_ws_new/
├── src/
│   ├── ackermann26_vehicle_description/
│   │   ├── urdf/
│   │   ├── launch/
│   │   ├── package.xml
│   │   └── CMakeLists.txt
│   │
│   └── ackermann26_vehicle_gazebo/
│       ├── launch/
│       ├── worlds/
│       ├── models/
│       ├── package.xml
│       └── CMakeLists.txt
│
├── build/
├── install/
└── log/


if not possible - copy-paste from GitHub!!
