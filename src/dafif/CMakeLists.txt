#********* Copyright © 2026 Jishnu Periya, Jonathon Bell. All rights reserved.
#**
#**  Purpose : CMake build script for the mixr_dafif library.
#**
#*****************************************************************************

file(GLOB_RECURSE MIXR_DAFIF_SOURCES "*.cpp")

add_library(mixr_dafif STATIC
  ${MIXR_DAFIF_SOURCES}
)

target_link_libraries(mixr_dafif PUBLIC
  mixr_base
)
