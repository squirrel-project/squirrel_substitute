cmake_minimum_required(VERSION 2.8.3)
project(robotino_arm_base_control)

## Find catkin macros and libraries
## if COMPONENTS list like find_package(catkin REQUIRED COMPONENTS xyz)
## is used, also find other catkin packages
find_package(catkin REQUIRED 
)

catkin_package(
)

## Declare a cpp executable
add_executable(robotino_arm_base_control_node
    src/robotino_arm_base_control_node.cpp)

