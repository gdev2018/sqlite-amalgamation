cmake_minimum_required(VERSION 3.14)
project(sqlite3am C)

set(CMAKE_C_STANDARD 11)

include_directories(.)


file(GLOB SOURCE_FILES
        shell.c
        sqlite3.c
        sqlite3.h
        sqlite3ext.h)

#add_executable(sqlite3am ${SOURCE_FILES})

add_library(sqlite3am SHARED ${SOURCE_FILES})