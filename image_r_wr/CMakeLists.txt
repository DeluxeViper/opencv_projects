cmake_minimum_required(VERSION 3.0)
cmake_policy(SET CMP0012 NEW)
PROJECT(image_r_wr)

set (CMAKE_CXX_STANDARD 11)

FIND_PACKAGE( OpenCV REQUIRED )
MESSAGE("OpenCV version : ${OpenCV_VERSION}")

include_directories(${OpenCV_INCLUDE_DIR})
link_directories(${OpenCV_LIB_DIR})

ADD_EXECUTABLE(${PROJECT_NAME} main.cpp)
TARGET_LINK_LIBRARIES(${PROJECT_NAME} ${OpenCV_LIBS})