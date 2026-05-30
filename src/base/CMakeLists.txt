#********* Copyright © 2026 Jishnu Periya, Jonathon Bell. All rights reserved.
#**
#**  Purpose : CMake build script for the mixr_base library.
#**
#*****************************************************************************

file(GLOB_RECURSE MIXR_BASE_SOURCES "*.cpp")
list(FILTER MIXR_BASE_SOURCES EXCLUDE REGEX ".*/osg/Matrix_implementation\\.cpp$")
if(WIN32)
  list(FILTER MIXR_BASE_SOURCES EXCLUDE REGEX ".*_linux\\.cpp$")
else()
  list(FILTER MIXR_BASE_SOURCES EXCLUDE REGEX ".*_msvc\\.cpp$")
  list(FILTER MIXR_BASE_SOURCES EXCLUDE REGEX ".*_mingw\\.cpp$")
endif()

add_library(mixr_base STATIC
  ${MIXR_BASE_SOURCES}
)

target_include_directories(mixr_base PUBLIC
  ${CMAKE_SOURCE_DIR}/include
  ${FREETYPE_INCLUDE_DIRS}
)

target_link_libraries(mixr_base PUBLIC
  Threads::Threads
  ${FREETYPE_LIBRARIES}
)

set_target_properties(mixr_base PROPERTIES
  OUTPUT_NAME mixr_base
)
