cmake_minimum_required(VERSION 3.0.2)
project(dnb_kemrox_custom_robot)

## Compile as C++11, supported in ROS Kinetic and newer
add_compile_options(-std=c++11)

## Find catkin macros and libraries
## if COMPONENTS list like find_package(catkin REQUIRED COMPONENTS xyz)
## is used, also find other catkin packages
find_package(catkin REQUIRED COMPONENTS
  roscpp
  rospy
)

################################################
## Declare ROS dynamic reconfigure parameters ##
################################################

catkin_package(
  #INCLUDE_DIRS include
  CATKIN_DEPENDS roscpp rospy
)

###########
## Build ##
###########

#include_directories(
#  include
#  ${catkin_INCLUDE_DIRS}
#)

#add_executable(dnb_kemrox_custom_robot_node
#    src/node.cpp
#)

#target_link_libraries(dnb_kemrox_custom_robot
#    ${catkin_LIBRARIES}
#)

#############
## Install ##
#############

## Mark executables and/or libraries for installation
#install(
#    TARGETS dnb_kemrox_custom_robot
#    RUNTIME DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
#)

## Mark other files for installation (e.g. launch and bag files, etc.)
install(DIRECTORY urdf DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION})
install(DIRECTORY meshes DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION})
install(DIRECTORY module_config DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION})
install(DIRECTORY launch DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION})