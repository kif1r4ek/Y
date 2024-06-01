cmake_minimum_required(VERSION 3.12)

set(PROJECT_NAME Y)

add_subdirectory(YCore)
add_subdirectory(YEditor)

set_property(DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR} PROPERTY VS_STARTUP_PROJECT YEditor)