#********* Copyright © 2026 Jishnu Periya, Jonathon Bell. All rights reserved.
#**
#**  Purpose : CMake build script for the mixr_simulation library.
#**
#*****************************************************************************

file(GLOB_RECURSE MIXR_SIMULATION_SOURCES "*.cpp")

add_library(mixr_simulation STATIC
  ${MIXR_SIMULATION_SOURCES}
)

target_link_libraries(mixr_simulation PUBLIC
  mixr_base
)
