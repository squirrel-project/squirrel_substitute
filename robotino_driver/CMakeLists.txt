cmake_minimum_required(VERSION 2.8.3)
project(robotino_driver)

## Find catkin macros and libraries
## if COMPONENTS list like find_package(catkin REQUIRED COMPONENTS xyz)
## is used, also find other catkin packages
find_package(catkin REQUIRED)
catkin_package()

###########
## Build ##
###########
add_executable(robotino_node src/robotino_node.cpp)
add_executable(robotino_odometry_node src/robotino_odometry_node.cpp)
add_executable(robotino_tilt_controller src/robotino_tilt_controller.cpp)

### INSTALL ###
install(TARGETS
  ARCHIVE DESTINATION ${CATKIN_PACKAGE_LIB_DESTINATION}
  LIBRARY DESTINATION ${CATKIN_PACKAGE_LIB_DESTINATION}
  RUNTIME DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)
