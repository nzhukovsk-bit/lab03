cmake_minimum_required(VERSION 3.10)

project(lab03 VERSION 1.0.0)

# Добавляем поддиректории с библиотеками
add_subdirectory(formatter_lib)
add_subdirectory(formatter_ex_lib)
add_subdirectory(solver_lib)

# Приложение hello_world (использует formatter_ex)
add_executable(hello_world hello_world.cpp)
target_link_libraries(hello_world
    formatter_ex
)

# Приложение solver (использует formatter_ex и solver_lib)
add_executable(solver solver.cpp)
target_link_libraries(solver
    formatter_ex
    solver_lib
)
