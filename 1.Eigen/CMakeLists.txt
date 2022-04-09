cmake_minimum_required(VERSION 3.10)
project(1_Eigen)
#find_package(OpenCV)

INCLUDE_DIRECTORIES(${OpenCV_INCLUDE_DIRS},
                    SYSTEM${CMAKE_CURRENT_SOURCE_DIR},
                    "/usr/include/eigen3")
add_subdirectory(Utils)
set(CMAKE_BUILD_TYPE Debug)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -Wall")
set(CMAKE_CXX_FLAGS  "${CMAKE_CXX_FLAGS} -g")
add_executable(1_Eigen main.cpp)
target_link_libraries(1_Eigen Utils)
