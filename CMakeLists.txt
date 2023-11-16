cmake_minimum_required(VERSION 3.15)

project(hello-world)
cmake_policy(SET CMP0057 NEW)

enable_testing()

include_directories(${CMAKE_CURRENT_BINARY_DIR})
file(WRITE generate/generated.h "#include <string> \n std::string version = \"v0.0.0\";")
add_executable(main src/main.cpp generate/generated.h)

message(FATAL_ERROR "FATAL ERROR from CMake")