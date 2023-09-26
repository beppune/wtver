cmake_minimum_required(VERSION 3.26)

project(wtver LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 20)

find_package(Boost COMPONENTS program_options)

message(STATUS ${Boost_INCLUDE_DIRS})
message(STATUS ${Boost_LIBRARIES})

add_executable(wtver main.cpp)
target_link_libraries(wtver libboost_program_options.a)

