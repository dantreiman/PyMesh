cmake_minimum_required(VERSION 3.11.0)
#set_property(GLOBAL PROPERTY RULE_LAUNCH_COMPILE "${CMAKE_COMMAND} -E time")

project(PyMesh)

include(Settings.cmake)
set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -DBOOST_BIND_GLOBAL_PLACEHOLDERS")

# Process code in each subdirectories
add_subdirectory(src)
add_subdirectory(tools)
add_subdirectory(python)

add_subdirectory(tests EXCLUDE_FROM_ALL)
#add_subdirectory(examples EXCLUDE_FROM_ALL)
