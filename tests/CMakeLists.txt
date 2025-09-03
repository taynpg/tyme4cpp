cmake_minimum_required(VERSION 3.30)

project(tests CXX)

if(MSVC)
    add_compile_options(/utf-8)
endif()

add_executable(tests tests.cpp)
target_link_libraries(tests tyme)
