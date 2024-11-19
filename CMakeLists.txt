cmake_minimum_required(VERSION 3.15...3.31)

project(HelloWorld)

  set(CMAKE_CXX_STANDARD 17
    CACHE 
    STRING "The C++ standard for the project")
  set(CMAKE_CXX_STANDARD_REQUIRED ON)
  set(CMAKE_CXX_EXTENSIONS OFF)


find_package(fmt CONFIG REQUIRED)

add_executable(HelloWorld helloworld.cpp)

target_link_libraries(HelloWorld PRIVATE fmt::fmt-header-only)
