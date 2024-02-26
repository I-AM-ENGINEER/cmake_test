cmake_minimum_required(VERSION 3.0)

project(test_lib)

set(SOURCE_LIB lib.c)

add_library(lib STATIC ${SOURCE_LIB})