cmake_minimum_required (VERSION 3.9)
include_directories(".")
add_subdirectory(katran)
if(DEFINED ENV{CMAKE_BUILD_EXAMPLE})
    message("Building example of thrift and grpc based katran server")
    add_subdirectory(example)
    add_subdirectory(example_grpc)
    message("Building tools/utils for katran")
    add_subdirectory(tools)
endif()
