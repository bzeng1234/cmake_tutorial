cmake_minimum_required(VERSION 3.10)

project(Tutorial VERSION 1.0)

#Create executable named "Tutorial" off of main.cc 
add_executable(Tutorial main.cc)

#Add subdirectory called "Adder" (Relative file path to this cmake directory)
add_subdirectory(Adder)

#include library directories to executable (Relative file path to this cmake directory)  
target_include_directories(Tutorial PUBLIC Adder/include)

#link directories to the target executable (Relative file path to this cmake directory)
target_link_directories(Tutorial PUBLIC Adder/include)

#link libraries to the target executable
target_link_libraries(Tutorial PUBLIC
    Adder
)