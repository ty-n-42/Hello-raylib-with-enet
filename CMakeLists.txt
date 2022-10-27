cmake_minimum_required(VERSION 3.20) # declare the minimum version of cmake required
project(cmake_with_dependencies C) # declare the project name and programming language
set(CMAKE_C_STANDARD_REQUIRED 11) # set the C standard to 2011

add_subdirectory(dependencies) # include ./dependencies/CMakeLists.txt
add_subdirectory(src) # include ./src/CMakeLists.txt
# the src sub-directory is where the project code resides