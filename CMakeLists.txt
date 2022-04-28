cmake_minimum_required(VERSION 3.22)


set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
include("cmake/HunterGate.cmake")


HunterGate(
        URL "https://github.com/ImDmitrybtw/hunter/archive/hv1.0.3.tar.gz"
        SHA1 "cfc4649d86e1377c371348bd7d42bccffdda5775"
)

project(lab07)

hunter_add_package(hello_foo)
find_package(hello_foo)

add_executable(lab07 main.cpp)
target_link_libraries(${PROJECT_NAME} hello_foo)

install(TARGETS ${PROJECT_NAME} RUNTIME DESTINATION bin)