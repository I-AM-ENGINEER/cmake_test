cmake_minimum_required(VERSION 3.22)

project(test_proj)

set(SOURCE_EXE src/main.c)

file(GLOB MY_SOURCES "${CMAKE_CURRENT_LIST_DIR}/src/*.c")

add_executable(app ${SOURCE_EXE})
target_sources(app PUBLIC ${MY_SOURCES})

include_directories(inc)

add_subdirectory(lib/lwrb)
add_subdirectory(lib/lwshell)

target_link_libraries(app lwrb lwshell)