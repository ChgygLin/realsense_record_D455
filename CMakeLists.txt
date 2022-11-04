cmake_minimum_required(VERSION 2.8)
project(recorder_realsense_D455)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")
add_definitions(-DCOMPILEDWITHC11)

find_package(OpenCV 4.4 REQUIRED)
find_package(realsense2 REQUIRED)
include_directories(${realsense2_INCLUDE_DIRS} ${OPENCV_INCLUDE_DIRS})

add_executable(${PROJECT_NAME} src/recorder_realsense_D455.cc)
target_link_libraries(${PROJECT_NAME} ${realsense2_LIBRARY} ${OpenCV_LIBS} )

