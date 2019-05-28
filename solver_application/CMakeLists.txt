cmake_minimum_required(VERSION 3.4)
project(solver_application)

set(CMAKE_CXX_STANDART 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/../solver_lib/ ${CMAKE_BINARY_DIR}/solver)
add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/../formatter_ex_lib/ ${CMAKE_BINARY_DIR}/formatter_ex)

add_executable(${CMAKE_PROJECT_NAME} ${CMAKE_CURRENT_SOURCE_DIR}/equation.cpp)

target_include_directories(${CMAKE_PROJECT_NAME}
    PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/../formatter_ex_lib/
           ${CMAKE_CURRENT_SOURCE_DIR}/../solver_lib/
)

target_link_libraries(${CMAKE_PROJECT_NAME} solver_lib formatter_ex)
