cmake_minimum_required(VERSION 3.30)

project(tyme CXX)

if(MSVC)
    add_compile_options(/utf-8)
    # set(CMAKE_WINDOWS_EXPORT_ALL_SYMBOLS ON)
endif()

add_library(tyme STATIC util.cpp tyme.cpp util.h tyme.h)
target_include_directories(tyme PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
