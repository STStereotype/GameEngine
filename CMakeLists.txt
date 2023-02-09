cmake_minimum_required(VERSION 3.5 FATAL_ERROR)
set(PROJECT_NAME "game-engine")
project(${PROJECT_NAME} LANGUAGES CXX)

message(STATUS "OS: ${CMAKE_CURRENT_LIST_DIR}")
# include directories
list(APPEND INCLUDE_DIRS "src")
list(APPEND INCLUDE_DIRS "include")

# source
list(APPEND SOURCES "src/main.cpp")

add_executable(${PROJECT_NAME} ${SOURCES})
target_include_directories(${PROJECT_NAME} PRIVATE ${INCLUDE_DIRS})

set_target_properties(${PROJECT_NAME} PROPERTIES RUNTIME_OUTPUT_DIRECTORY_DEBUG ${CMAKE_CURRENT_LIST_DIR}/bin/Debug)
set_target_properties(${PROJECT_NAME} PROPERTIES RUNTIME_OUTPUT_DIRECTORY_RELEASE ${CMAKE_CURRENT_LIST_DIR}/bin/Release)
