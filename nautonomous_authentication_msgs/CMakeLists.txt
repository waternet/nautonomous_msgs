cmake_minimum_required(VERSION 2.8.3)
project(nautonomous_authentication_msgs)

find_package(catkin REQUIRED COMPONENTS
  message_generation
  std_msgs
)

add_service_files(
  FILES
  Authentication.srv
  Encryption.srv
)

generate_messages(
  DEPENDENCIES
  std_msgs
)

catkin_package(
  CATKIN_DEPENDS message_runtime
)
set(CMAKE_INCLUDE_CURRENT_DIR ON)

include_directories(
  include
  ${catkin_INCLUDE_DIRS}
)