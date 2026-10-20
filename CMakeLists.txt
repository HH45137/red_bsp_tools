cmake_minimum_required(VERSION 3.20)

project(red_bsp_tools LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/bin")

if (MSVC)
    add_compile_definitions(_CRT_SECURE_NO_WARNINGS _CRT_NONSTDC_NO_DEPRECATE)
    add_compile_options(/utf-8 /W3)
endif ()

if (NOT WIN32)
    message(FATAL_ERROR "red_bsp_tools only supports Windows builds (MSVC).")
endif ()

add_subdirectory(common)
add_subdirectory(utils/qrad)
