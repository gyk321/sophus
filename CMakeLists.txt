cmake_minimum_required(VERSION 3.24)
project(useSophus)

#find_package(Sophus REQUIRED)
set(CMAKE_BUILD_TYPE "Debug")
set(Sophus_INCLUDE_DIRS /usr/include/Sophus/sophus)
set(SOPHUS_LIBRARIES /usr/include/Sophus/build/libSophus.so)
set(ALL_CODE_LIST Sophus.cpp)

MESSAGE(STATUS "sophus include: " ${Sophus_INCLUDE_DIRS})
MESSAGE(STATUS "sophus lib: " ${SOPHUS_LIBRARIES})
add_subdirectory(src bin)
include_directories(${Sophus_INCLUDE_DIRS})