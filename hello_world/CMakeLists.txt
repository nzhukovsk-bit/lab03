cmake_minimum_required(VERSION 3.10)

project(hello_world VERSION 1.0.0)

add_executable(hello_world
    main.cpp
)

target_link_libraries(hello_world
    formatter_ex
)

# Добавляем путь к заголовочным файлам formatter_ex
target_include_directories(hello_world PRIVATE
    ${CMAKE_SOURCE_DIR}/formatter_ex_lib
)

set_target_properties(hello_world PROPERTIES
    CXX_STANDARD 11
    CXX_STANDARD_REQUIRED ON
)
