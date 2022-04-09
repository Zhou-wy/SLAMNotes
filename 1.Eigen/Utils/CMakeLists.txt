CMAKE_MINIMUM_REQUIRED(VERSION 3.10)
SET(UTILS_LIN_SRC
        Src/eigenMatrix.cpp
        Src/eigenGeometry.cpp)
INCLUDE_DIRECTORIES(${OpenCV_INCLUDE_DIRS},
                    SYSTEM${CMAKE_CURRENT_SOURCE_DIR},
                    "/usr/include/eigen3")
                    
#create our new utils lib
ADD_LIBRARY(Utils ${UTILS_LIN_SRC})
#make sure the compiler can find the include files for our library
TARGET_INCLUDE_DIRECTORIES(Utils PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/include)
