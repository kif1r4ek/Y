cmake_minimum_required(VERSION 3.12)

set(ENGINE_PROJECT_NAME YCore)

add_library(${ENGINE_PROJECT_NAME} STATIC
	scr/YCore/Utils/test.cpp
	includes/YCore/Utils/test.hpp
)

target_include_directories(${ENGINE_PROJECT_NAME} PUBLIC includes)
target_compile_features(${ENGINE_PROJECT_NAME} PUBLIC cxx_std_17)

add_subdirectory(../external/glfw ${CMAKE_CURRENT_BINARY_DIR}/glfw)
target_link_libraries(${ENGINE_PROJECT_NAME} PRIVATE glfw)
