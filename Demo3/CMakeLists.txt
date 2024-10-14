cmake_minimum_required(VERSION 2.8)
project(demo3)
add_subdirectory(math)# 添加一个子目录 ，子目录里有我们的静态库
aux_source_directory(. dir)

add_executable(demo ${dir})
target_link_libraries(demo MATH)