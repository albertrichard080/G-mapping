# G-mapping
First Run the fake_odom_pub.py if you are going to use the lidar as odometry.
After running that provide a static transform tf using the command
rosrun tf static_transform_publisher 0 0 0 0 0 0 odom base_link 80
