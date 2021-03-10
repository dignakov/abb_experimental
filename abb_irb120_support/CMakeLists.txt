cmake_minimum_required(VERSION 3.5)

project(abb_irb120_support)

if(NOT CMAKE_CXX_STANDARD)
  set(CMAKE_CXX_STANDARD 14)
endif()

if(CMAKE_COMPILER_IS_GNUCXX OR CMAKE_CXX_COMPILER_ID MATCHES "Clang")
  add_compile_options(-Wall -Wextra)
endif()

# find dependencies
find_package(ament_cmake REQUIRED)

#if (CATKIN_ENABLE_TESTING)
  #find_package(roslaunch REQUIRED)
  #roslaunch_add_file_check(tests/roslaunch_test.xml)
#endif()

install(
  DIRECTORY config launch meshes urdf
  DESTINATION share/${PROJECT_NAME}
)

ament_package()

