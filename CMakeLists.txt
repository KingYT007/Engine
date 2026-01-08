cmake_minimum_required(VERSION 3.10)
project(Engine)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Add the GLFW library from the libs directory
add_subdirectory(libs/GLFW)

# Create the executable for your project
add_executable(Engine src/main.cpp)

# Link the GLFW library to your executable
# This also pulls in any necessary system libraries like OpenGL
target_link_libraries(Engine PRIVATE glfw)
