cmake_minimum_required(VERSION 3.10)
project(MyProject)

set(CMAKE_CXX_STANDARD 14)

find_package(GLEW REQUIRED)
find_package(glfw3 3.3 REQUIRED)
find_package(OpenGL REQUIRED)

add_executable(main main.cpp)

target_link_libraries(main GLEW::GLEW glfw)
target_link_libraries(main ${OPENGL_gl_LIBRARY})