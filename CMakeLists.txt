cmake_minimum_required(VERSION 3.16)

project(HttpServerProject)

set(CMAKE_CXX_STANDARD 17)

find_package(Boost REQUIRED COMPONENTS system)

add_executable(server
    src/main.cpp
    src/utils.cpp
)

target_include_directories(server PRIVATE include)

target_link_libraries(server PRIVATE Boost::system)
