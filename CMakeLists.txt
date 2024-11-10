cmake_minimum_required(VERSION 3.10)

project(test_simulation)

set(CMAKE_CXX_FLAGS "")
set(CMAKE_EXPORT_COMPILE_COMMANDS "1")

include_directories(
    includes
)

link_directories(
    /usr/local/lib
)

file(GLOB SOURCES (
    srcs/*.cpp
))

add_executable(
    ${PROJECT_NAME}
    ${SOURCES}
)

target_link_libraries(
    ${PROJECT_NAME}
    -lncurses
)