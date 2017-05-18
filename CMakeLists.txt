cmake_minimum_required(VERSION 2.8)
project(heartbeat C CXX)

set(PROJECT_MAJOR_VERSION 1)
set(PROJECT_MINOR_VERSION 0)
set(PROJECT_PATCH_VERSION 0)
set(PROJECT_VERSION ${PROJECT_MAJOR_VERSION}.${PROJECT_MINOR_VERSION}.${PROJECT_PATCH_VERSION})

set(CMAKE_CXX_FLAGS ${CMAKE_CXX_FLAGS} "-fPIC -std=c++11")
set(CMAKE_C_FLAGS ${CMAKE_C_FLAGS} "-fPIC") 

option(BUILD_TEST "build unit test" OFF)

include_directories(include)
add_subdirectory(src)

if(BUILD_TEST) 
    add_subdirectory(unit_test)
endif()    
