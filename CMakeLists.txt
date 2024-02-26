cmake_minimum_required(VERSION 3.0)

project(test_proj)

set(SOURCE_EXE main.c)

include_directories(lib)

add_executable(app ${SOURCE_EXE})

add_subdirectory(lib)

target_link_libraries(app lib)