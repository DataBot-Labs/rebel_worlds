cmake_minimum_required(VERSION 3.5)
project(rebel_worlds)

find_package(ament_cmake REQUIRED)
find_package(ros_gz_sim REQUIRED)

install(
  DIRECTORY launch models worlds 
  DESTINATION share/${PROJECT_NAME}
)

ament_environment_hooks("${CMAKE_CURRENT_SOURCE_DIR}/env-hooks/rebel_worlds.dsv.in")

ament_export_dependencies(ament_cmake)
ament_export_dependencies(ros_gz_sim)

ament_package()
