cmake_minimum_required(VERSION 3.10.2)
project(poo2_pc1_2021_0)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_CURRENT_BINARY_DIR}/${OUTPUT_DEBUG})
if(UNIX AND NOT APPLE)
    set(CMAKE_CXX_FLAGS -pthread)
endif()

add_executable(poo2_pc1_2021_0
        main.cpp
        global.h
        test_1.cpp
        test_2.cpp
        test_3.cpp
        p1.h p1.cpp
        p2.h p2.cpp
        p3.h p3.cpp
        polynomial.h polynomial.cpp
        standard_deviation.h
        filter.h  )

configure_file(test_1.in ${CMAKE_RUNTIME_OUTPUT_DIRECTORY} COPYONLY)
configure_file(test_2.in ${CMAKE_RUNTIME_OUTPUT_DIRECTORY} COPYONLY)
configure_file(test_3.in ${CMAKE_RUNTIME_OUTPUT_DIRECTORY} COPYONLY)
