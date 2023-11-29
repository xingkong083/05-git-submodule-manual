cmake_minimum_required(VERSION 3.21)
project(GitSubmoduleManual CXX)

add_executable(main main.cpp)
configure_file(config.yaml config.yaml COPYONLY)

add_subdirectory(extern/yaml-cpp)
target_link_libraries(main PRIVATE yaml-cpp)

