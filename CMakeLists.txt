cmake_minimum_required (VERSION 3.5)
project (DataFrame_tester)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_BUILD_TYPE Debug) # Defualt built type
set(CMAKE_EXPORT_COMPILE_COMMANDS ON) # Get compilation database if available

# Dataframe config config
find_package(DataFrame REQUIRED)
include_directories( ${DataFrame_INCLUDE_DIRS} ) # Cmake find me header files

add_executable(dataframe_tester dataframe_tester.cc)
target_link_libraries(dataframe_tester DataFrame::DataFrame) # Cmake link me libraries
