cmake_minimum_required(VERSION 3.10)
project(Engine)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_subdirectory(libs/GLFW)
add_subdirectory(libs/glad)

add_executable(Engine src/main.cpp)

target_link_libraries(Engine PRIVATE glfw)
target_link_libraries(Engine PRIVATE glad)
