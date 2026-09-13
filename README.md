## Ackermann Vehicle Simulation

ROS 2 and Gazebo simulation of the Ackermann vehicle, including the vehicle description, sensors, Gazebo simulation, and ROS 2 control interfaces.

## Requirements

The simulation requires:

- Ubuntu
- ROS 2
- Gazebo
- colcon
- ros_gz_sim
- xacro

---

## Structure

The workspace has the following folder structure:

``` 
sm26_ws_new/
├── src/
│   ├── ackermann26_vehicle_description/
│   │   ├── urdf/
│   │   ├── launch/
│   │   ├── package.xml
│   │   └── CMakeLists.txt
│   │
│   └── ackermann26_vehicle_gazebo/
│       ├── config/
│       ├── launch/
│       ├── package.xml
│       └── CMakeLists.txt

``` 

---

## Open a terminal:

``` 
cd ~/Workspaces/sm26_ws_new
colcon build --symlink-install
source install/setup.bash
``` 
---

## Launch 

ros2 launch ackermann26_vehicle_gazebo gz_sim_launch.py


## Check Topics

ros2 topic list

For example to see Lidar output topic:
ros2 topic echo /scan


## Keyboard Control
Open a second terminal.
(Because I didn't manage to implement the keyboard in the general launch file.)

ros2 run teleop_twist_keyboard teleop_twist_keyboard
Keyboard controls with
U  I  O
J  K  L
M  <  >

## End simulation
Ctrl + C

##Clean Build

rm -rf build install log
colcon build --symlink-install
source install/setup.bash

