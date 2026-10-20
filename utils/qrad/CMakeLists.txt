add_executable(qrad
    lightmap.cpp
    qrad.cpp
    trace.cpp
    vismat.cpp
)

target_include_directories(qrad PRIVATE "${CMAKE_CURRENT_SOURCE_DIR}")
target_link_libraries(qrad PRIVATE bsp_common)
