cmake_minimum_required(VERSION 3.1...3.29)

project(ImGui LANGUAGES CXX)

add_library(ImGui STATIC
        imgui.cpp
        imgui_draw.cpp
        imgui_tables.cpp
        imgui_widgets.cpp
        backends/imgui_impl_glfw.cpp
        backends/imgui_impl_opengl3.cpp
        misc/cpp/imgui_stdlib.cpp
)

target_include_directories(ImGui PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
target_link_libraries(ImGui PUBLIC glfw)

