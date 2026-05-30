#********* Copyright © 2026 Jishnu Periya, Jonathon Bell. All rights reserved.
#**
#**  Purpose : CMake build script for the mixr_ighost_pov library.
#**
#*****************************************************************************

file(GLOB_RECURSE MIXR_IGHOST_POV_SOURCES "*.cpp")

add_library(mixr_ighost_pov STATIC
  ${MIXR_IGHOST_POV_SOURCES}
)

target_link_libraries(mixr_ighost_pov PUBLIC
  mixr_base
  mixr_models
)
