cmake_minimum_required(VERSION 3.1.0)
# minimum version required

project(HelloWorld)
# project name, otherwise we will get "default" name

add_executable(basic HelloWorld.cpp)
# add executable target with name "basic" with *.cpp source

set(CMAKE_INSTALL_PREFIX ${CMAKE_CURRENT_SOURCE_DIR}/Build)
# set the CMAKE_INSTALL_PREFIX, DESTINATION path is relative to ${CMAKE_INSTALL_PREFIX}

if (UNIX)
  install(TARGETS basic DESTINATION bin)
  # DESTINATION path is relative to CMAKE_INSTALL_PREFIX
  # Need to set the CMAKE_INSTALL_PREFIX to get the DESTINATION path
  # install path
endif()
