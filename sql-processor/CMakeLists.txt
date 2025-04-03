cmake_minimum_required(VERSION 2.9.10)
set(CMAKE_CXX_STANDARD 11)
project(SQLProcessor C CXX)

# sql-parser
set(CMAKE_PREFIX_PATH ${CMAKE_CURRENT_SOURCE_DIR}/../../third-party/sql-parser/lib)
find_library(SQL_PARSER_LIB NAMES libsqlparser.so)

aux_source_directory(. DIR_LIB_SRCS)


add_library(SQLProcessor ${DIR_LIB_SRCS})


target_link_libraries(SQLProcessor ${SQL_PARSER_LIB})

