cmake_minimum_required (VERSION 3.8)
set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} "${CMAKE_SOURCE_DIR}/cmake_modules")
project (midas_to_tof)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)


# set up output paths for executable binaries
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${PROJECT_BINARY_DIR}/bin)


find_package(ROOT REQUIRED)


add_executable(midas_to_tof
        common_types.h
        main.cpp)

target_link_libraries(midas_to_tof PRIVATE ${ROOT_LIBRARIES})

