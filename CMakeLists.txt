cmake_minimum_required(VERSION 3.0)

set(PROJECT_NAME "employee_test")

project(${PROJECT_NAME} VERSION 1.0.0 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED TRUE)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall -Wextra -Wpedantic -Wshadow -Wundef -Wno-missing-field-initializers")
include_directories(include)
#file(GLOB SOURCES . "${CMAKE_CURRENT_SOURCE_DIR}/src/*.cpp")
file(GLOB SOURCES "src/*.cpp")
message(${SOURCES})
add_executable(${PROJECT_NAME} ${SOURCES})

