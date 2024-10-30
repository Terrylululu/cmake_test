aux_source_directory(. libfile)
add_library(Mathlib ${libfile})

install(TARGETS Mathlib DESTINATION  ${PROJECT_BINARY_DIR}/lib)
install(FILES MathFunctions.h  DESTINATION  ${PROJECT_BINARY_DIR}/include)