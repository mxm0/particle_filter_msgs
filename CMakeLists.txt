cmake_minimum_required(VERSION 2.8.3)
project(particle_filter_msgs)

find_package(catkin REQUIRED COMPONENTS
  message_generation
  rospy
	geometry_msgs
	std_msgs
)

## Generate messages in the 'msg' folder
add_message_files(
  FILES
	ParticleCloud.msg
)

## Generate added messages and services with any dependencies listed here
generate_messages(
  DEPENDENCIES
  std_msgs geometry_msgs  # Or other packages containing msgs
)

catkin_package(
	CATKIN_DEPENDS message_runtime std_msgs geometry_msgs
)
