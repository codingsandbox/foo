cmake_minimum_required(VERSION 3.12)
project(foo)

include(cmake/deps.cmake)

file(GLOB SOURCES CONFIGURE_DEPENDS "src/*.c")

add_library(foo STATIC ${SOURCES})

target_include_directories(foo PUBLIC "inc/")
