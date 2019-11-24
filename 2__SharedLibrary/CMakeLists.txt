cmake_minimum_required(VERSION 3.1.8)
# minimum version required

project(SharedLibrary)
# project name, otherwise we will get "default" name

add_library(MySharedLib SHARED SharedLib.cpp)
# add a library target called "MySharedLib" to be built from the
# source files listed in the command invocation.

add_executable(Main main.cpp)
# add executable target with name "Main" with *.cpp source

target_link_libraries(Main MySharedLib)
#Specify libraries or flags to use when linking a given target.
