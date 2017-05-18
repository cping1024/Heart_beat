cmake_minimum_required(VERSION 2.8)

file(GLOB_RECURSE src *.cpp)
add_library(heart_beat SHARED ${src})
set_target_properties(heart_beat PROPERTIES VERSION ${PROJECT_VERSION} SOVERSION ${PROJECT_MAJOR_VERSION})
install(TARGETS heart_beat DESTINATION lib)
