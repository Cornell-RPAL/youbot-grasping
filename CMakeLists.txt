cmake_minimum_required(VERSION 2.8.3)
project(youbot_grasping)
find_package(catkin REQUIRED COMPONENTS message_generation rospy std_msgs geometry_msgs
  youbot_manipulation vicon_bridge)
add_service_files(
  DIRECTORY srv
  FILES Pickup.srv Putdown.srv
)

generate_messages()

catkin_package(
  CATKIN_DEPENDS message_runtime
)
