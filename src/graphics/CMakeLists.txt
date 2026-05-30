#********* Copyright © 2026 Jishnu Periya, Jonathon Bell. All rights reserved.
#**
#**  Purpose : CMake build script for the mixr_graphics library.
#**
#*****************************************************************************

find_package(OpenGL REQUIRED)

file(GLOB_RECURSE MIXR_GRAPHICS_SOURCES "*.cpp")
list(FILTER MIXR_GRAPHICS_SOURCES EXCLUDE REGEX ".*/fonts/ftgl/.*\\.cpp$")

add_library(mixr_graphics STATIC
  ${MIXR_GRAPHICS_SOURCES}
)

target_link_libraries(mixr_graphics PUBLIC
  mixr_base
  OpenGL::GL
)

find_package(FTGL QUIET)
if(FTGL_FOUND)
  add_subdirectory(fonts/ftgl)
endif()
