cmake_minimum_required(VERSION 3.22)
project(lab07)

set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
include("cmake/HunterGate.cmake")


HunterGate(
        URL "https://github.com/"
        SHA1 ""
)

hunter_add_package(hello_foo)
find_package(hello_foo)

add_executable(lab07 main.cpp)
target_link_libraries(${PROJECT_NAME} hello_foo)

install(TARGETS ${PROJECT_NAME} DESTINATION bin)