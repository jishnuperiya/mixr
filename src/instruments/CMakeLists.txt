#********* Copyright © 2026 Jishnu Periya, Jonathon Bell. All rights reserved.
#**
#**  Purpose : CMake build script for the mixr_instruments library.
#**
#*****************************************************************************

file(GLOB_RECURSE MIXR_INSTRUMENTS_SOURCES "*.cpp")

add_library(mixr_instruments STATIC
  ${MIXR_INSTRUMENTS_SOURCES}
)

target_link_libraries(mixr_instruments PUBLIC
  mixr_base
  mixr_graphics
)
