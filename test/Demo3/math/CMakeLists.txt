aux_source_directory(. libfile)#将所有的文件放进libfile 中
add_library(mathlib ${libfile})#生成lib  库文件，libfile 被引用要加${}