cmake_minimum_required(VERSION 3.13)
project(tosutil)

set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/lib)
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)

set(CMAKE_CXX_STANDARD 17)

add_executable(tosutil main.cpp)

add_subdirectory(src)
target_link_libraries(tosutil PUBLIC util_lib)
