cmake_minimum_required(VERSION 3.10)

project(Tutorial VERSION 1.0)

add_executable(Tutorial main.cc)

add_subdirectory(Adder)

target_include_directories(Tutorial PUBLIC Adder/include)

target_link_directories(Tutorial PUBLIC Adder/include)

target_link_libraries(Tutorial PUBLIC
    Adder
)