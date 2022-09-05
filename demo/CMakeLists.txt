cmake_minimum_required(VERSION 3.15.0)

project(demo)

#.h and lib_dir
include_directories(${PROJECT_SOURCE_DIR}/hwlib/include)
link_directories(${PROJECT_SOURCE_DIR}/hwlib/lib/)

#lib
add_executable(main_static src/main.c)
target_link_libraries(main_static hwlib_static)

#dll
add_executable(main_shared src/main.c)
target_link_libraries(main_shared hwlib_shared)