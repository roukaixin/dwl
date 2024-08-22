cmake_minimum_required(VERSION 3.29)
project(dwl C)

set(VERSION 0.7)
add_definitions(-DVERSION="${VERSION}")

set(CMAKE_C_STANDARD 99)

include_directories(/usr/include/wlroots-0.18 /usr/include/pixman-1 /usr/include/fcft ${PROJECT_SOURCE_DIR})

set(SRC dwl.c util.c)

add_definitions(-DWLR_USE_UNSTABLE)

add_executable(dwl ${SRC})