# Necessary to set CMake minimum version (3.1 needed for Spike):
cmake_minimum_required(VERSION 3.1 FATAL_ERROR)

# Spike needs C++11:
set (CMAKE_CXX_STANDARD 11)
set (CMAKE_CXX_STANDARD_REQUIRED ON)

# Don't want to build Spike examples:
set(BUILD_EXAMPLES OFF CACHE BOOL "Do not build Spike examples")

# Need to build Spike from the submodule:
add_subdirectory(Spike)

# Make Spike headers available:
include_directories(BEFORE SYSTEM "${PROJECT_SOURCE_DIR}/Spike")

# Add CPUTest executable:
add_executable(CPUTest CPUTest.cpp)

# And link CPUTest to Spike:
target_link_libraries(CPUTest Spike)


