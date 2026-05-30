#********* Copyright © 2026 Jishnu Periya, Jonathon Bell. All rights reserved.
#**
#**  Purpose : CMake build script for the mixr_ighost_flightgear library.
#**
#*****************************************************************************

file(GLOB_RECURSE MIXR_IGHOST_FG_SOURCES "*.cpp")

add_library(mixr_ighost_flightgear STATIC
  ${MIXR_IGHOST_FG_SOURCES}
)

target_link_libraries(mixr_ighost_flightgear PUBLIC
  mixr_base
  mixr_models
)
