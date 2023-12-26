cmake_minimum_required(VERSION 3.14.4)

project(poco-example)

include(FetchContent)
FetchContent_Declare(
  Poco
  URL https://github.com/pocoproject/poco/archive/refs/tags/poco-1.12.5p2-release.zip
)
FetchContent_MakeAvailable(Poco)

add_executable(pocoex main.cpp)
target_link_libraries(pocoex PUBLIC Poco::Foundation)
