cmake_minimum_required(VERSION 3.16)
project(ServerCode LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(BOOST_ROOT "/opt/homebrew/opt/boost")
find_package(Boost REQUIRED)

add_executable(ServerCode Server.cpp)

target_include_directories(ServerCode PRIVATE ${Boost_INCLUDE_DIRS})
target_link_libraries(ServerCode PRIVATE pthread)