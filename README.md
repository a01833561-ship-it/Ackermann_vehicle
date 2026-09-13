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

---

## 1. Workspace Structure

The workspace has the following structure:

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

Open a terminal:

```bash
cd ~/Workspaces/sm26_ws_new
source /opt/ros/$ROS_DISTRO/setup.bash
colcon build --symlink-install
source install/setup.bash

Launch

Run the Gazebo simulation:

ros2 launch ackermann26_vehicle_gazebo <launch_file>.launch.py

Replace <launch_file> with the launch file in:

src/ackermann26_vehicle_gazebo/launch/

Keyboard Control

Open a second terminal:

source /opt/ros/$ROS_DISTRO/setup.bash
source ~/Workspaces/sm26_ws_new/install/setup.bash
ros2 run teleop_twist_keyboard teleop_twist_keyboard

Check Topics

ros2 topic list

For example:

ros2 topic echo /imu/data
ros2 topic echo /scan

Clean Build

If necessary:

cd ~/Workspaces/sm26_ws_new
rm -rf build install log
colcon build --symlink-install
source install/setup.bash


└── log/


if not possible - copy-paste from GitHub!!
