cmake_minimum_required(VERSION 3.12)
project(hmap2obj VERSION 1.0 LANGUAGES CXX C)

SET(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -pthread -ldl")

add_subdirectory(lodepng)
add_subdirectory(obj)
add_subdirectory(hmap2obj)