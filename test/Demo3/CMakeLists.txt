cmake_minimum_required(VERSION 3.10)
add_subdirectory(math)# 将math文件夹的内容加入构建（说明这个文件夹有一个 cmakelist）
aux_source_directory(. mainfile)
add_executable(DEMO ${mainfile})
target_link_libraries(DEMO mathlib) 