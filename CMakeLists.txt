cmake_minimum_required(VERSION 3.31 FATAL_ERROR)

project(Engine)

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)

add_executable(Engine src/main.cpp)

set(SFML_DIR include/SFML-2.6.2)
target_link_libraries(Engine sfml-graphics)

set(CMAKE_MODULE_PATH "${CMAKE_CURRENT_LIST_DIR}/cmake_modules")
find_package(SFML 2.6 REQUIRED graphics network audio window system)

