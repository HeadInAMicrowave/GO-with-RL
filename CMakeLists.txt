cmake_minimum_required(VERSION 3.6.0)
project(rl_go VERSION 1.0.0)
cmake_policy(SET CMP0072 NEW)

find_package(OpenGL REQUIRED)

add_executable(rl_go 
    src/config.hpp 
    src/main.cpp 
    src/glad.c
)

target_include_directories(rl_go PRIVATE dependencies)

find_package(glfw3 REQUIRED)
target_link_libraries(rl_go glfw3 OpenGL::GL)