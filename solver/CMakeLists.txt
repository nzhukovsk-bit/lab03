cmake_minimum_required(VERSION 3.10)

project(solver VERSION 1.0.0)

add_executable(solver
    main.cpp
)

target_link_libraries(solver
    formatter_ex
    solver_lib
)

set_target_properties(solver PROPERTIES
    CXX_STANDARD 11
    CXX_STANDARD_REQUIRED ON
)
