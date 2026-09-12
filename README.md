opening rviz -> first go to Workspaces/sm26/src
colcon build --symlink-install
-> creates a link to current source file - only if its in a new file/folder so it saves there
cd sm26_ws
source install/setup.bash -> tells OS that we installed new package - use in every new ubuntu terminal
	ros2 pkg list | grep Ackermann
	-> check if it's there
ros2 launch ackermann26_vehicle_description display.launch.py

For Gazebo:
. Workspaces/sm26_ws/install/setup.bash
gz sim -> opens an empty terminal and keeps running
ros2 run ros_gz_sim create -topic /robot_description

ros2 launch urdf_tutorial display.launch.py model:=home/sina/mobile_robot_base.urdf -> should start the simulation in rviz ?
rs
ssh -> connect to device

cd Workspaces/sm26_ws/src/ackermann26_vehicle_description/urdf/
code mobile_robot_base.urdf
-> open the code in visual studio code

sudo -> access to superuser
sudo poweroff	or	wsl --shutdown 	or Stop-Computer
-> turn off ubuntu bzw. computer 

sudo apt install terminator
sudo apt update -> obs
git clone https://github.... -> download all the folders into ubuntu

echo $DISPLAY -> trying to remove Error, echo subscribes to a topic and shows the info
glxheads -> should show visual output


mkdir folder_name -> create new directory
ls -> list
cd folder_name -> change dir in a subfolder	or	cd . -> for topfolder 	or	cd ~
touch file_name.py -> creates a file
rm file_name -> deletes
rm -rf -> removes a full folder recursive force
--help -> documentation
ls -a -> list including hidden carpets
mkdir.file_name -> hidden create

ros2 run demo_nodes_py -> talker
ros2 topic pub /chatter std_msgs/msg/String'data__'
ros2 node list -> see all active nodes
ros2 node info./node_name -> see what a node does
bw -> bandwidth of topic
delay -> measure the delay
find 
pub -> publish a message to a topic
info
type

Powershell should be Version 2.7.13
Laptop had gazebo version ignition, PC im Lab hat die neuere gz sim mit jazzy


launch description()
rviz_config_path = os.pathjoin(robot_description_pkg,
rviz, ...
-> make an empty file called? in the launch order  then download from canvas
always compile with
colcon build --symlink-install

ubuntu: using xacro
ros2 run ros_gz_sim create --help
-> we want to pass the car model into the gazebo 
ros2 run ros_gz_sim create -topic robot_description ??...

to-do:
<plugin> "gz::sim::systems::AckermannSteering" filename="gz-sym-ackermann-steering-system">
copy <topic> from documentation (many)

in base.urdf -> xacro:include filename ... urdf/mobile_robot.gazebo

ros2 run xacro xacro src/ackermann26_vehicle_description/urdf/the_first_vehicle.urdf.xacro
 gz topic -t /model/the_first_vehicle/odometry
ros2 run roz_gz_bridge parameter_bridge config_file:=home/sina/Workspaces/sm26_ws/src/ackerman26_vehicle_description/config/ros_bridge.yaml

--Homework--

Bridge Homework: passes commands between ROS and Gazebo
-> go to sdformat.org  /specification / sensor / inside a <gazebo> tab put the /sensors attributes (green) in base.xacro
<sensor name="csi_fron_camera" type="camera">
and open the attributes?mean Elements? (blue) 
<always_on>true>/always_on>
adding ALL THE COMMON AND Specific properties if they are Required:1 
Also find the one for steering?

if not possible - copy-paste from GitHub!!
