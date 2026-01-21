cmake_minimum_required(VERSION 3.4.3)

project(lodepng)

if(WIN32)
    set(CMAKE_WINDOWS_EXPORT_ALL_SYMBOLS ON)
    add_compile_options(/wd4267)
    add_compile_options(/wd4334)
endif()

add_library(lodepng-static STATIC lodepng/lodepng.h lodepng/lodepng.cpp)
add_library(lodepng SHARED lodepng/lodepng.h lodepng/lodepng.cpp)

set_target_properties(lodepng PROPERTIES PUBLIC_HEADER lodepng/lodepng.h)

install(
    TARGETS
        lodepng lodepng-static
    RUNTIME DESTINATION bin
    LIBRARY DESTINATION lib
    ARCHIVE DESTINATION lib
    PUBLIC_HEADER DESTINATION
        include
)
