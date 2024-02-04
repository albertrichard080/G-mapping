# G-mapping-Readme

# Introduction

G-mapping is a ROS-compatible mapping tool designed for robotic applications. The following steps outline the setup process for utilizing G-mapping with an RPLidar sensor.

# Prerequisites
Before starting, ensure you have the necessary permissions for the RPLidar sensor's port. Run the following command to grant permission:

bash

    sudo chmod 666 /dev/ttyUSB0

Replace /dev/ttyUSB0 with the correct port based on your system.

# Launching RPLidar
 Navigate to your ROS workspace directory. In the provided example:

bash

    cd ~/richard/src/rplidar_ros/launch/

Launch the RPLidar node using the appropriate launch file. In this case, we use rplidar.launch:

bash

    roslaunch rplidar.launch

Ensure the RPLidar initializes successfully and note the assigned serial port.
# Launching G-mapping

Open a new terminal and navigate to the ROS workspace directory:

bash

    cd ~/richard/src/rplidar_ros/launch/

Run the fake_odom_pub.py script to publish the fake odometry node from lidar: <--only use when your using lidar as for odometry data-->

bash

    rosrun rplidar_ros fake_odom_pub.py

To provide a static transform using the rosrun tf command:

bash

    rosrun tf static_transform_publisher 0 0 0 0 0 0 odom base_link 80

Finally, launch G-mapping using the appropriate launch file, for instance:

bash

    roslaunch gmapping_map.launch

# Launching Map Saver
To save the map run the following command:

bash

    rosrun map_server map_saver -f map
Ensure the sequence is followed meticulously for accurate mapping results. Refer to the ROS documentation or community forums for troubleshooting or additional information.
# Additional Notes

Make sure to replace /dev/ttyUSB0 with the correct port assigned to your RPLidar.
Adjust file paths based on your ROS workspace structure.
Consult RPLidar and G-mapping documentation for further customization and troubleshooting.
