cmake_minimum_required(VERSION 3.22)
project(IDS)

set(CMAKE_CXX_STANDARD 20)

add_compile_options(-Wall -Wextra -pedantic)

find_package(OpenCV REQUIRED)
include_directories(${OpenCV_INCLUDE_DIRS})

include_directories(include/)
add_executable(ids src/main.cpp
        src/devices/Camera.cpp
        src/devices/Laser.cpp)
target_link_libraries(ids ${OpenCV_LIBS})