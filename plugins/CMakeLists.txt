cmake_minimum_required(VERSION 2.6)
project(BetaflightPlugin)

find_package(gazebo REQUIRED)

include_directories(include ${GAZEBO_INCLUDE_DIRS})
link_directories(${GAZEBO_LIBRARY_DIRS})
list(APPEND CMAKE_CXX_FLAGS ${GAZEBO_CXX_FLAGS})

add_library(BetaflightPlugin SHARED BetaflightPlugin.cc)
target_link_libraries(BetaflightPlugin ${GAZEBO_LIBRARIES})
