#********* Copyright © 2026 Jishnu Periya, Jonathon Bell. All rights reserved.
#**
#**  Purpose : CMake build script for the mixr_graphics_ftgl library.
#**
#*****************************************************************************

file(GLOB_RECURSE MIXR_FTGL_SOURCES "*.cpp")

add_library(mixr_graphics_ftgl STATIC
  ${MIXR_FTGL_SOURCES}
)

target_include_directories(mixr_graphics_ftgl PUBLIC
  ${FTGL_INCLUDE_DIRS}
)

target_link_libraries(mixr_graphics_ftgl PUBLIC
  mixr_graphics
  ${FTGL_LIBRARIES}
  ${FREETYPE_LIBRARIES}
)
