可以使用如下的 步骤：
mkdir build 
cd  build 
cmake .. 
cmake --build . --target install

# 注意这里的安装的exe文件是 静态的 ，静态库通常通过 add_library(MyLib STATIC ...) 创建。
如果没有使用 SHARED 关键字，那么库将是静态链接的。
