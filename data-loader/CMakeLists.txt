cmake_minimum_required(VERSION 2.9.10)
set(CMAKE_CXX_STANDARD 11)
project(DataLoader C CXX)

aux_source_directory(. DIR_LIB_SRCS)

add_library(DataLoader ${DIR_LIB_SRCS})
