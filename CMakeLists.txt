# CMakeLists.txt
cmake_minimum_required(VERSION 3.0)
project(test)

find_package(SDL2 CONFIG REQUIRED)
find_package(imgui CONFIG REQUIRED)

add_executable(main main.cpp
imgui_impl_sdl2.cpp
imgui_impl_sdlrenderer.cpp)

target_link_libraries(main PRIVATE
SDL2::SDL2main
SDL2::SDL2
#SDL2::SDL2-static
imgui::imgui
)
