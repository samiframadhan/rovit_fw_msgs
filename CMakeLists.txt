cmake_minimum_required(VERSION 3.0.2)
project(rovit_fw_msgs)

find_package(catkin REQUIRED COMPONENTS
  geometry_msgs
  std_msgs
  message_generation
)


add_message_files(
  DIRECTORY msg
  FILES
  PID.msg
  Rovit.msg
  RovitDebug.msg
)

generate_messages(
  DEPENDENCIES
  geometry_msgs
  std_msgs
)

catkin_package(
  CATKIN_DEPENDS geometry_msgs std_msgs
)