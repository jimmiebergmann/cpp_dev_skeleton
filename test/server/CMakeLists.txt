project(server_tests)

enable_language(C CXX)


set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -g -O0") # debug, no optimisation
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} --coverage") # enabling coverage

include_directories(../../include/server)

add_executable(
    server_tests
    server_tests.cpp
    ../../source/server/Balancer.cpp
    )
