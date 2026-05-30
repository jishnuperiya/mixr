#********* Copyright © 2026 Jishnu Periya, Jonathon Bell. All rights reserved.
#**
#**  Purpose : CMake build script for the mixr_interop_dis library.
#**
#*****************************************************************************

file(GLOB_RECURSE MIXR_DIS_SOURCES "*.cpp")

add_library(mixr_interop_dis STATIC
  ${MIXR_DIS_SOURCES}
)

target_link_libraries(mixr_interop_dis PUBLIC
  mixr_base
  mixr_interop
  mixr_models
  mixr_simulation
)
