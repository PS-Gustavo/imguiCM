
cmake_minimum_required(VERSION 3.4...3.20 FATAL_ERROR)

project(imgui VERSION 3.4.0 LANGUAGES CXX)

add_library(imgui STATIC
    ./imgui/imgui.cpp
)
target_include_directories(imgui PUBLIC
    ./imgui/imgui/
)
set_property(
    TARGET imgui
    PROPERTY POSITION_INDEPENDENT_CODE ON
)