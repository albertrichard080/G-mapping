# G-mapping-Readme
Introduction

G-mapping is a mapping tool designed to work with ROS (Robot Operating System). To ensure proper functionality, follow the steps below.
Getting Started

    rosrun fake_odom_pub.py 

if utilizing lidar as odometry.

Provide a static transform using the rosrun tf command.

bash

    rosrun tf static_transform_publisher 0 0 0 0 0 0 odom base_link 80

Ensure that these steps are executed in the specified order to achieve accurate mapping results. For any issues or additional information, refer to the ROS documentation or community forums.
