cmake_minimum_required(VERSION 3.23)

set(CMAKE_TOOLCHAIN_FILE
  ${CMAKE_SOURCE_DIR}/vcpkg/scripts/buildsystems/vcpkg.cmake
  CACHE STRING "Vcpkg toolchain file"
)

project(ash-tree LANGUAGES CXX VERSION 0.0.1)

find_package(navidson CONFIG REQUIRED)

add_executable(descend)
target_sources(descend PRIVATE descend.cpp)
target_link_libraries(descend PRIVATE nvr::house)
