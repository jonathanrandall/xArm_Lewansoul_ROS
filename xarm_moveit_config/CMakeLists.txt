cmake_minimum_required(VERSION 3.5)
project(xarm_moveit_config)

# Default to C++14
if(NOT CMAKE_CXX_STANDARD)
  set(CMAKE_CXX_STANDARD 14)
endif()

find_package(ament_cmake REQUIRED)

install(
  DIRECTORY config launch
  DESTINATION share/${PROJECT_NAME}
)

install(
  FILES .setup_assistant
  DESTINATION share/${PROJECT_NAME}
)

ament_package()
