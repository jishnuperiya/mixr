#********* Copyright © 2026 Jishnu Periya, Jonathon Bell. All rights reserved.
#**
#**  Purpose : CMake build script for the mixr_map_vpf library.
#**
#*****************************************************************************

file(GLOB_RECURSE MIXR_MAP_VPF_SOURCES "*.cpp")

add_library(mixr_map_vpf STATIC
  ${MIXR_MAP_VPF_SOURCES}
)

target_link_libraries(mixr_map_vpf PUBLIC
  mixr_base
)
