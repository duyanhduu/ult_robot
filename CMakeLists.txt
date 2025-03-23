cmake_minimum_required(VERSION 3.0.2)
project(mobile_robot)

# Find catkin macros and libraries
find_package(catkin REQUIRED COMPONENTS
  
  rospy
  std_msgs
  urdf
  xacro
  
)

# Declare a catkin package
catkin_package(
  CATKIN_DEPENDS  rospy std_msgs urdf xacro
)

# Specify additional locations of header files
include_directories(
  ${catkin_INCLUDE_DIRS}
)

# Install directories
install(DIRECTORY meshes rviz urdf
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
) 