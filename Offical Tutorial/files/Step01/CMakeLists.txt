cmake_minimum_required(VERSION 3.10)

set(CMAKE_EXPORT_COMPILE_COMMANDS True)

# Get the latest abbreviated commit hash of the working branch
execute_process(
  COMMAND git log -1 --format=%h
  WORKING_DIRECTORY ${CMAKE_CURRENT_LIST_DIR}
  OUTPUT_VARIABLE GIT_HASH
  OUTPUT_STRIP_TRAILING_WHITESPACE)

# set the project name and version
project(Tutorial VERSION 1.0)
set(Tutorial_VERSION_PATCH g${GIT_HASH})

configure_file(TutorialConfig.h.in TutorialConfig.h)

# add the executable
add_executable(Tutorial tutorial.cxx)

target_include_directories(Tutorial PUBLIC "${PROJECT_BINARY_DIR}")
