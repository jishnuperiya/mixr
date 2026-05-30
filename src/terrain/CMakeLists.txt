#********* Copyright © 2026 Jishnu Periya, Jonathon Bell. All rights reserved.
#**
#**  Purpose : CMake build script for the mixr_terrain library.
#**
#*****************************************************************************

file(GLOB_RECURSE MIXR_TERRAIN_SOURCES "*.cpp")

add_library(mixr_terrain STATIC
  ${MIXR_TERRAIN_SOURCES}
)

target_link_libraries(mixr_terrain PUBLIC
  mixr_base
)
