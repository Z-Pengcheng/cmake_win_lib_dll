cmake_minimum_required(VERSION 3.15.0)
project(hwlib)

include_directories(${CMAKE_SOURCE_DIR}/include)
add_library(hwlib_static STATIC src/lib.c)
add_library(hwlib_shared SHARED src/lib.c)

install(TARGETS hwlib_static hwlib_shared)
install(FILES ${CMAKE_SOURCE_DIR}/include/lib.h DESTINATION include)