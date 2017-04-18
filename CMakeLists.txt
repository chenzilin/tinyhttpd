project(tinyhttpd)
cmake_minimum_required(VERSION 2.8)
aux_source_directory(. DIR_SRCS)
add_executable(tinyhttpd ${DIR_SRCS})

set (SRC_VERSION_MAJOR 0)
set (SRC_VERSION_MINOR 1)
set (SRC_VERSION_PATCH 0)
set (SRC_VERSION ${SRC_VERSION_MAJOR}.${SRC_VERSION_MINOR}.${SRC_VERSION_PATCH})
set (PROJECT_VERSION "${SRC_VERSION}")

target_link_libraries(tinyhttpd pthread)

install(TARGETS tinyhttpd DESTINATION bin)
