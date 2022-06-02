cmake_minimum_required(VERSION 3.21)
project(PRG2-Template C)

set(CMAKE_C_STANDARD 17)
set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS}")
set(CMAKE_C_STANDARD_REQUIRED ON)


if (CMAKE_BUILD_TYPE MATCHES Debug)
    add_definitions(-DDEBUG=1)
    set(CMAKE_C_FLAGS_DEBUG "-g -O0")
    add_compile_options(-fdiagnostics-show-location=every-line)
else ()
    set(CMAKE_C_FLAGS_RELEASE "-O3")
    add_compile_options(-Werror)
endif ()

add_compile_options(-Wall)
add_compile_options(-Wextra)
add_compile_options(-Wconversion)
add_compile_options(-Wsign-conversion)
add_compile_options(-Wshadow)
add_compile_options(-Wvla)
add_compile_options(-Wparentheses)
add_compile_options(-Wpedantic)
add_compile_options(-Wunused)
add_compile_options(-pedantic)
add_compile_options(-fdiagnostics-color=always)

add_executable(PRG2-Template main.c)
# Link math.h
# target_link_libraries(PRG2-Template m)
