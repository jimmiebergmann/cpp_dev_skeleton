cmake_minimum_required(VERSION 2.8 FATAL_ERROR)
project (doforward)

set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/lib)
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/lib)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/bin)

# Recurse into the "Hello" and "Demo" subdirectories. This does not actually
# cause another cmake executable to run. The same process will walk through
# the project's entire directory structure.
add_subdirectory (${PROJECT_SOURCE_DIR}/source/server)
add_subdirectory (${PROJECT_SOURCE_DIR}/source/bin/server)
add_subdirectory (${PROJECT_SOURCE_DIR}/test/server)
#add_subdirectory (Demo)


