cmake_minimum_required(VERSION 2.8.3)
project(simple_media_msgs)

find_package(catkin REQUIRED COMPONENTS
  message_generation std_msgs
)

## Generate msgs in the 'msg' folder
add_message_files(
  DIRECTORY msg
  FILES
  ShowVideo.msg
  )

generate_messages(
  DEPENDENCIES
  std_msgs  # Or other packages containing msgs
)

catkin_package(
  CATKIN_DEPENDS message_runtime std_msgs
)
