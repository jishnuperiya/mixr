#********* Copyright © 2026 Jishnu Periya, Jonathon Bell. All rights reserved.
#**
#**  Purpose : CMake build script for the mixr_map_rpf library.
#**
#*****************************************************************************

file(GLOB_RECURSE MIXR_MAP_RPF_SOURCES "*.cpp")

add_library(mixr_map_rpf STATIC
  ${MIXR_MAP_RPF_SOURCES}
)

target_link_libraries(mixr_map_rpf PUBLIC
  mixr_base
  mixr_graphics
)
