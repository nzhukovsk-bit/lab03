cmake_minimum_required(VERSION 3.10)

project(solver_lib VERSION 1.0.0)

add_library(solver_lib STATIC
    solver.cpp
)

target_include_directories(solver_lib PUBLIC
    ${CMAKE_CURRENT_SOURCE_DIR}
)

# Подключаем математическую библиотеку (для sqrtf)
target_link_libraries(solver_lib
    m
)
