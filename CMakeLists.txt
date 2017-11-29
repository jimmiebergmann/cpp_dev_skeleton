cmake_minimum_required(VERSION 2.8 FATAL_ERROR)
project (doforward)

set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/lib)
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/lib)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/bin)

# Tests

# Tests - Server

#add_definitions(-std=c++11)

set(SERVER_SOURCES  source/server/Balancer.cpp)
set(SERVER_TESTS_SOURCES  test/server/server_tests.cpp)



add_executable(server_tests ${SERVER_SOURCES} ${SERVER_TESTS_SOURCES})
target_include_directories(server_tests PUBLIC include/server)
target_compile_options(server_tests PUBLIC --coverage )
target_link_libraries(server_tests PUBLIC gcov)
