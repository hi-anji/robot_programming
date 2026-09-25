cmake_minimum_required(VERSION 2.8.3)
project(mini_core)

set(CMAKE_CXX_STANDARD 11) #use c++ 11 standard
set(CMAKE_CXX_FLAGS "-Wall -Wextra -pedantic") #adds warnings

# TODO invokes the routines to find a package called Eigen3
#add eigen3, make headers available
find_package(Eigen3 REQUIRED) #find eigen3
include_directories(${EIGEN3_INCLUDE_DIR}) #add eigen3 headers

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/src) #headers in src reachable from every subfolder

# add project source code
add_subdirectory(src)

# TODO do the same for executables
add_subdirectory(executables)