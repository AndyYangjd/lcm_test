cmake_minimum_required(VERSION 3.23)
project(lcm_test)

set(CMAKE_CXX_STANDARD 20)

find_package(lcm REQUIRED)
include_directories(lcm)

add_executable(lcm_receive lcm_receive.cpp)
target_link_libraries(lcm_receive
        lcm)

add_executable(lcm_send lcm_send.cpp)
target_link_libraries(lcm_send
        lcm)

add_executable(read_log read_log.cpp)
target_link_libraries(read_log
        lcm)

