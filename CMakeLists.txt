cmake_minimum_required(VERSION 3.20)

project(SaveDDS)

set(CMAKE_CXX_STANDARD 17)

add_library(SaveDDS STATIC "")
target_include_directories(SaveDDS PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})

target_compile_definitions(SaveDDS PRIVATE CRT_SECURE_NO_WARNINGS)

target_sources(SaveDDS
    PRIVATE
        "savedds.cpp"
        "stb_dxt.h"

    PUBLIC
        "savedds.h"
)
