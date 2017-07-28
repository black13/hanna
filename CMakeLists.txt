cmake_minimum_required(VERSION 3.9)
enable_testing()


FILE(GLOB SOURCES *.cpp)

FOREACH(name IN LISTS SOURCES)
    GET_FILENAME_COMPONENT(exname ${name} NAME_WE)
    ADD_EXECUTABLE(${exname} ${name})
ENDFOREACH()

