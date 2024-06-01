cmake_minimum_required(VERSION 3.12)

set(EDITOR_PROJECT_NAME YEditor)

add_executable(${EDITOR_PROJECT_NAME}
	scr/main.cpp
)

target_link_libraries(${EDITOR_PROJECT_NAME} YCore)
target_compile_features(${EDITOR_PROJECT_NAME} PUBLIC cxx_std_17)

set_target_properties(${EDITOR_PROJECT_NAME} PROPERTIES 
	RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin/
)