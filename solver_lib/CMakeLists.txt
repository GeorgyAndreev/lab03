cmake_minimum_required(VERSION 3.4)
project(solver_lib)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(SOURCES ${CMAKE_CURRENT_SOURCE_DIR}/solver.cpp)
set(HEADERS ${CMAKE_CURRENT_SOURCE_DIR}/solver.h)

add_library(solver_lib ${SOURCES})

target_include_directories(solver_lib PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/)
