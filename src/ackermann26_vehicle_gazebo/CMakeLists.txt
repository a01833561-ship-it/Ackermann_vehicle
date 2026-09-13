cmake_minimum_required(VERSION 3.8)
project(ackermann26_vehicle_gazebo)

if(CMAKE_COMPILER_IS_GNUCXX OR CMAKE_CXX_COMPILER_ID MATCHES "Clang")
  add_compile_options(-Wall -Wextra -Wpedantic)
endif()

# find dependencies
find_package(ament_cmake REQUIRED)
# find_package(<dependency> REQUIRED)
find_package(ament_cmake REQUIRED)

INSTALL(
  DIRECTORY config launch 
  DESTINATION share/${PROJECT_NAME}
)

if(BUILD_TESTING)
  find_package(ament_lint_auto REQUIRED)
  
  set(ament_cmake_cpplint_FOUND TRUE)
  ament_lint_auto_find_test_dependencies()
endif()

# gemini to compile sensors_worlds?
#install(DIRECTORY launch worlds DESTINATION share/${PROJECT_NAME})


ament_package()
