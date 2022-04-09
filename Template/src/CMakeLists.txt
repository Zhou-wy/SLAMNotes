cmake_minimum_required(VERSION 3.20)
PROJECT(Template)
SET(SRC_LIST main.cpp)
INCLUDE_DIRECTORIES(${PROJECT_SOURCE_DIR}/include,
                    "/usr/local/include/Eigen")
MESSAGE(STATUS "This is BINARY dir " ${HELLO_BINARY_DIR})
MESSAGE(STATUS "This is SOURCE dir "${HELLO_SOURCE_DIR})
ADD_EXECUTABLE(Template ${SRC_LIST})
