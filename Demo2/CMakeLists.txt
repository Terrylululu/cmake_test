#cmake_minimum_required(VERSION 3.0)
#project(Demo2)
#add_executable(demo main.cc  MathFunctions.cc)



cmake_minimum_required(VERSION 3.0)
project(Demo2)
aux_source_directory(. DIR)
add_executable(demo ${DIR})