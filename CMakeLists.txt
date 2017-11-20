cmake_minimum_required(VERSION 3.0)

set(CMAKE_CXX_STANDARD 11)

include(cmake/HunterGate.cmake)

HunterGate(URL "https://github.com/nex-7/hunter/archive/v0.19.137.1.tar.gz" SHA1 "0a8badad8c0112ce52a81fb1f20f8585803265b6")

project(cget)

hunter_add_package(CURL)
find_package(CURL CONFIG REQUIRED)

add_executable(cget ${CMAKE_CURRENT_SOURCE_DIR}/cget.cpp)
target_link_libraries(cget CURL::libcurl)

install(TARGETS cget RUNTIME DESTINATION bin)
