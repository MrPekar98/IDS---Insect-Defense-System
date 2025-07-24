cmake_minimum_required(VERSION 3.28)
project(IDS)

set(CMAKE_CXX_STANDARD 20)

include_directories(include/)
add_executable(ids src/main.cpp)
