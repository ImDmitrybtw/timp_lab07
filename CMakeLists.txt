cmake_minimum_required(VERSION 3.22)


set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
include("cmake/HunterGate.cmake")


HunterGate(
        URL "https://github.com/ImDmitrybtw/hunter/archive/hfv1.0.0.tar.gz"
        SHA1 "0186fecdae35d4aa4d4d1b9db851fa166563e9b9"
)

project(lab07)

hunter_add_package(hello_foo)
find_package(hello_foo)

add_executable(lab07 main.cpp)
target_link_libraries(${PROJECT_NAME} hello_foo)

install(TARGETS ${PROJECT_NAME} DESTINATION bin)