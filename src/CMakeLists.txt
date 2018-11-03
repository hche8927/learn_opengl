cmake_minimum_required(VERSION 2.4)
project(LearnOpenGL)

set(GLFW_BUILD_DOCS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_TESTS OFF CACHE BOOL "" FORCE)
set(GLFW_BUILD_EXAMPLES OFF CACHE BOOL "" FORCE)
add_subdirectory(${PROJECT_SOURCE_DIR}/lib/glfw)

add_executable(HelloWorld WIN32
    ${PROJECT_SOURCE_DIR}/
        HelloWorld.cpp
        glad.c
)

target_include_directories(HelloWorld PRIVATE ${PROJECT_SOURCE_DIR}/include/)

target_link_libraries(HelloWorld glfw)