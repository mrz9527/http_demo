cmake_minimum_required(VERSION 3.5)

project(httpserver)
add_definitions(-std=c++11)

set(LIBEVENT_HOME ${PROJECT_BINARY_DIR}/libevent)
include_directories(${LIBEVENT_HOME}/include)
link_directories(${LIBEVENT_HOME}/lib)

add_executable(httpserver myhttpServer.cpp)
target_link_libraries(httpserver event)
