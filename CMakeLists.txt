cmake_minimum_required(VERSION 3.0.0)
set(CMAKE_BUILD_TYPE "")

project(yolov5)

find_package(OpenCV REQUIRED)

add_executable(yolov5 yolov5.cpp)


include_directories(${OpenCV_INCLUDE_DIRS})
target_link_libraries(yolov5 ${OpenCV_LIBS} ${CMAKE_THREAD_LIBS_INIT})
