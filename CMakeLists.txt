cmake_minimum_required(VERSION 3.30)
project(tyme4cpp LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

if(MSVC)
    add_compile_options(/utf-8)
endif()

add_subdirectory(tyme)
add_subdirectory(tests)
enable_testing()
add_test(NAME tyme_test COMMAND tests)
