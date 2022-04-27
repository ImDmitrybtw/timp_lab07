cmake_minimum_required(VERSION 3.22)


set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
include("cmake/HunterGate.cmake")


HunterGate(
        URL "https://github.com/ImDmitrybtw/hunter/archive/hfv1.0.2.tar.gz"
        SHA1 "e5517c73fc9fc7da81e35027162c007c70df0cf4"
)

project(lab07)

hunter_add_package(hello_foo)
find_package(hello_foo)

add_executable(lab07 main.cpp)
target_link_libraries(${PROJECT_NAME} hello_foo)

install(TARGETS ${PROJECT_NAME} RUNTIME DESTINATION bin)