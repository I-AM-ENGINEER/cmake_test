cmake_minimum_required(VERSION 3.0)

project(test_proj)

set(SOURCE_EXE main.c)

include_directories(lib/lwrb)

add_executable(app ${SOURCE_EXE})

add_subdirectory(lib/lwrb)

target_link_libraries(app lib/lwrb)