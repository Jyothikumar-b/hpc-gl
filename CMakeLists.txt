cmake_minimum_required(VERSION 3.5.0)
project(VIZ CXX)

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/deps/glew-2.1.0-win32/glew-2.1.0/include)
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/deps/glfw-3.4.bin.WIN64/include)

add_executable(VIZ src/triangle.cpp)

target_link_libraries(VIZ opengl32.lib)
target_link_libraries(VIZ ${CMAKE_CURRENT_SOURCE_DIR}/deps/glew-2.1.0-win32/glew-2.1.0/lib/Release/x64/glew32.lib)
target_link_libraries(VIZ ${CMAKE_CURRENT_SOURCE_DIR}/deps/glfw-3.4.bin.WIN64/lib-mingw-w64/libglfw3.a)
