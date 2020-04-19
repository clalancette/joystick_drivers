cmake_minimum_required(VERSION 3.0.5)
project(wiimote_msgs)

find_package(catkin REQUIRED COMPONENTS geometry_msgs message_generation)

add_message_files(
  DIRECTORY msg
  FILES IrSourceInfo.msg State.msg TimedSwitch.msg)

generate_messages(DEPENDENCIES geometry_msgs)

catkin_package(
  CATKIN_DEPENDS geometry_msgs message_runtime
)
