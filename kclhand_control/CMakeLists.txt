cmake_minimum_required(VERSION 2.8.3)
project(kclhand_control)

## Find catkin macros and libraries
## if COMPONENTS list like find_package(catkin REQUIRED COMPONENTS xyz)
## is used, also find other catkin packages
find_package(catkin REQUIRED)
catkin_package()

###########
## Build ##
###########
add_executable(HelloEposCmd src/HelloEposCmd.cpp)
add_executable(motor_move src/motor_move.cpp)
add_executable(motor_move_velocity src/motor_move_velocity.cpp)
add_executable(move_to_position_hand src/move_to_position_hand.cpp)
add_executable(move_to_position_hand2 src/move_to_position_hand2.cpp)
add_executable(hand_current_control src/hand_current_control.cpp)
add_executable(state_publisher src/state_publisher.cpp)
add_executable(motor_pub src/motor_pub.cpp)
add_executable(hand2_lower_sphere_parallel_grasp src/hand2_lower_sphere_parallel_grasp.cpp)

# for the hand2 eigengrasp hand2_lower_sphere_central grasp
add_executable(hand2_lower_sphere_central_grasp src/hand2_lower_sphere_central_grasp.cpp)
# for the hand2 eigengrasp hand2_lower_sphere_cylinder grasp
add_executable(hand2_lower_sphere_cylinder_grasp src/hand2_lower_sphere_cylinder_grasp.cpp)
# for the hand2 eigengrasp hand2_upper_sphere_cylinder grasp
add_executable(hand2_upper_sphere_cylinder_grasp src/hand2_upper_sphere_cylinder_grasp.cpp)
# for the hand2 eigengrasp hand2_upper_sphere_central grasp
add_executable(hand2_upper_sphere_central_grasp src/hand2_upper_sphere_central_grasp.cpp)
# for the hand2 eigengrasp hand2_upper_sphere_parallel grasp
add_executable(hand2_upper_sphere_parallel_grasp src/hand2_upper_sphere_parallel_grasp.cpp)
# switch hemi-sphere from lower to upper
add_executable(hand2_switch_to_upper_sphere src/hand2_switch_to_upper_sphere.cpp)
# for the hand2 grasp
add_executable(hand2_grasp src/hand2_grasp.cpp)

# switch hemi-sphere from upper to lower
add_executable(hand2_switch_to_lower_sphere src/hand2_switch_to_lower_sphere.cpp)
add_executable(hand2_reset_position src/hand2_reset_position.cpp)
add_executable(metaHand src/metaHand.cpp)
add_executable(metahand_control src/metahand_control.cpp)
add_executable(controller_metahand src/metaHand_controller.cpp)
add_executable(wien_controller_metahand src/Metahand_vienna_controller.cpp)
add_executable(controller_metahand_v2 src/Metahand_controller_v2.cpp)
add_executable(controller_metahand_ca src/metahand_controller_calibration.cpp)
add_executable(controller_metahand_review src/metahand_controller_cali_new.cpp)
add_dependencies(controller_metahand kclhand_control_generate_messages_cpp)
### INSTALL ###
install(TARGETS
  ARCHIVE DESTINATION ${CATKIN_PACKAGE_LIB_DESTINATION}
  LIBRARY DESTINATION ${CATKIN_PACKAGE_LIB_DESTINATION}
  RUNTIME DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)
