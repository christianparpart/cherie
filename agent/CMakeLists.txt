cmake_minimum_required(VERSION 2.8)
project(cherie-agent)

include(FindPkgConfig)
include(FindDoxygen)
include(CheckIncludeFiles)
include(CheckFunctionExists)
include(CheckVariableExists)
include(CheckTypeSize)
include(CheckLibraryExists)
include(CheckCSourceCompiles)
include(CMakeDetermineCCompiler)

add_definitions(-pthread)
add_definitions(-std=c++0x)

add_executable(cherie-agent main.cpp)
#target_link_libraries(cherie-agent XzeroBase XzeroHttp)

install(TARGETS cherie-agent RUNTIME DESTINATION sbin)
install(FILES agent.conf DESTINATION etc)
