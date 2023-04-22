
cmake_minimum_required(VERSION 3.4...3.20 FATAL_ERROR)

project(imgui VERSION 3.4.0 LANGUAGES CXX)

add_library(imgui STATIC
    ./imgui/imgui.cpp
    ./imgui/imgui_demo.cpp
    ./imgui/imgui_draw.cpp
    ./imgui/imgui_tables.cpp
    ./imgui/imgui_widgets.cpp    
)
target_include_directories(imgui PUBLIC
    ./imgui/
    ./imgui/backends/
)
set_property(
    TARGET imgui
    PROPERTY POSITION_INDEPENDENT_CODE ON
)