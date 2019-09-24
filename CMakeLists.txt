cmake_minimum_required (VERSION 3.5)
project (DataFrame_tester)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_BUILD_TYPE Debug) # Defualt built type
set(CMAKE_EXPORT_COMPILE_COMMANDS ON) # Get compilation database if available

# Dataframe config config
find_package(DataFrame REQUIRED)
include_directories( ${DataFrame_INCLUDE_DIRS} )

# add_executable(dataframe_tester dataframe_tester.cc)
add_executable(vectors_tester vectors_tester.cc)
