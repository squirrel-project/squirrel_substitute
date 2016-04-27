cmake_minimum_required(VERSION 2.8.3)
project(cf_control)

## Find catkin macros and libraries
## if COMPONENTS list like find_package(catkin REQUIRED COMPONENTS xyz)
## is used, also find other catkin packages
find_package(catkin REQUIRED 
)

## Declare a cpp executable
add_executable(cf_control_node
    src/cf_control_node.cpp
)

