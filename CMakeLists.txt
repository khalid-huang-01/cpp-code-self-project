cmake_minimum_required(VERSION 3.14)
project(cpp_demo_02)

set(CMAKE_CXX_STANDARD 17)

aux_source_directory(. DIRSRCS)
include_directories(./ ./hello ./world)
add_subdirectory(hello)
add_subdirectory(world)

add_executable(helloworld ${DIRSRCS} hello/hello.cpp hello/hello.h world/world.cpp)
target_link_libraries(helloworld hello world)
