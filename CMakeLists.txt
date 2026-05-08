cmake_minimum_required(VERSION 3.10)

project(lab03 VERSION 1.0.0)

# Добавляем подпроекты
add_subdirectory(formatter_lib)
add_subdirectory(formatter_ex_lib)
add_subdirectory(solver_lib)
add_subdirectory(hello_world)
add_subdirectory(solver)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
# ========== НАСТРОЙКА CPACK ==========
include(InstallRequiredSystemLibraries)

set(CPACK_PACKAGE_NAME "solver")
set(CPACK_PACKAGE_VERSION "1.0.0")
set(CPACK_PACKAGE_DESCRIPTION_SUMMARY "Quadratic equation solver")
set(CPACK_PACKAGE_VENDOR "Student Name")
set(CPACK_PACKAGE_CONTACT "your.email@example.com")

# Указываем, какой исполняемый файл устанавливать
install(TARGETS solver DESTINATION bin)

# Настройка для DEB и RPM
set(CPACK_DEBIAN_PACKAGE_ARCHITECTURE "amd64")
set(CPACK_RPM_PACKAGE_RELEASE "1")

# Генерируем пакеты: DEB, RPM, TGZ (для Linux)
set(CPACK_GENERATOR "DEB;RPM;TGZ")

include(CPack)
