cmake_minimum_required(VERSION 3.2.0)
project(BA)

SET(CMAKE_SYSTEM_NAME Linux)
SET(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${PROJECT_SOURCE_DIR}/build/bin)	        # 设置了Debug版本和Release版本可执行文件的输出目录
SET(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/build/bin)			        # 设置可执行文件的输出目录
SET(LIBRARY_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/build/lib)			        # 设置库文件的输出目录

find_package(Eigen3 REQUIRED)
include_directories(${EIGEN3_INCLUDE_DIR})
add_subdirectory(${PROJECT_SOURCE_DIR}/bal)
add_subdirectory(${PROJECT_SOURCE_DIR}/ceres)