cmake_minimum_required(VERSION 3.10)
project(OpenGLTriangle)

set(CMAKE_CXX_STANDARD 17)
find_package(OpenGL REQUIRED)
find_package(GLEW REQUIRED)
find_package(glfw3 3.3 REQUIRED)

set(SOURCE_FILES test.cpp glad.c)




add_executable(test ${SOURCE_FILES})
target_link_libraries(test OpenGL::GL GLEW::GLEW glfw)

