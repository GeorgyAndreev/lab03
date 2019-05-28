cmake_minimum_required(VERSION 3.4)
project(formatter)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(SOURCES ${CMAKE_CURRENT_SOURCE_DIR}/formatter.cpp)

add_library(formatter STATIC ${SOURCES})

target_include_directories(formatter PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
