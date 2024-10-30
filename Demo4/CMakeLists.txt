cmake_minimum_required(VERSION 3.10)
#在cmake 配置项目的时候会，可以用到
option(USE_MYMATH "Use provided math implementation" ON)
#set(USE_MYMATH ON)  #仅仅在cmakelist 程序中用到
#需要加双引号，代表路径
configure_file("${PROJECT_SOURCE_DIR}/config.h.in"  "${PROJECT_BINARY_DIR}/config.h")

if(USE_MYMATH)
 add_subdirectory(${PROJECT_SOURCE_DIR}/math)
 include_directories(${PROJECT_SOURCE_DIR}/math)
 set(EXTRA_lib Mathlib)
endif(USE_MYMATH)
include_directories(${PROJECT_BINARY_DIR})
aux_source_directory(. all_main_file)
add_executable(DEMO ${all_main_file})
target_link_libraries(DEMO ${EXTRA_lib})