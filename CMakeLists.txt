cmake_minimum_required(VERSION 3.0)

project(ryu)

set(CMAKE_CXX_STANDARD 11)

add_library(ryu ryu/d2s.c ryu/f2s.c ryu/d2fixed.c ryu/s2d.c ryu/s2f.c)
target_include_directories(ryu PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
set_target_properties(ryu PROPERTIES
    INTERFACE_INCLUDE_DIRECTORIES ${CMAKE_CURRENT_SOURCE_DIR})
