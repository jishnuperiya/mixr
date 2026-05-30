cmake_minimum_required(VERSION 3.20.2)

project(mixr
  VERSION     1.0.0
  LANGUAGES   CXX
)

set(CMAKE_CXX_STANDARD          17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS        OFF)

find_package(Threads  REQUIRED)
find_package(Freetype REQUIRED)

add_subdirectory(src/base)
add_subdirectory(src/dafif)
add_subdirectory(src/linkage)
add_subdirectory(src/simulation)
add_subdirectory(src/terrain)
add_subdirectory(src/models)
add_subdirectory(src/graphics)
add_subdirectory(src/instruments)
add_subdirectory(src/interop)
add_subdirectory(src/ighost)
add_subdirectory(src/map)
add_subdirectory(src/recorder)
add_subdirectory(src/ui)
