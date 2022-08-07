#include header files to directory
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/include)
#add all source files to library called Adder (will create library object called libAdder.a)
add_library(Adder src/adder.cc)