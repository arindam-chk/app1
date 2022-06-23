project(app1)
cmake_minimum_required(VERSION 3.0)
enable_testing()

add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/core_submodule ${CMAKE_CURRENT_SOURCE_DIR}/core_submodule/build)
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/core_submodule/src)
add_executable(run_x86_64 src/app.cc)
target_link_libraries(run_x86_64 core_submodule)
