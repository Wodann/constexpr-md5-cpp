cmake_minimum_required(VERSION 3.0)

project(constexpr_md5 VERSION 0.1.0 LANGUAGES CXX)

add_library(constexpr_md5 INTERFACE IMPORTED GLOBAL)
set_target_properties(constexpr_md5 PROPERTIES
    INTERFACE_INCLUDE_DIRECTORIES ${CMAKE_CURRENT_SOURCE_DIR}/include
)

enable_testing()
add_subdirectory(test)