add_library(bsp_common STATIC
    bspfile.cpp
    cmdlib.cpp
    mathlib.cpp
    polylib.cpp
    scriplib.cpp
    threads.cpp
)

target_include_directories(bsp_common PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}")
