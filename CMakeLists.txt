cmake_minimum_required(VERSION 2.8)
set(PROJECT_NAME wfs)
project(PROJECT_NAME)
find_package(Threads)
add_definitions(-Wall -D_REENTRANT -D_GNU_SOURCE -D_UNICODE -g -Os)

add_executable(example_http example_http_client.cpp)
set_target_properties(example_http PROPERTIES COMPILE_FLAGS "-std=c++1y")
target_link_libraries(example_http ${CMAKE_THREAD_LIBS_INIT})
