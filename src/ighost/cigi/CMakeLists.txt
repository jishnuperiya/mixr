#********* Copyright © 2026 Jishnu Periya, Jonathon Bell. All rights reserved.
#**
#**  Purpose : CMake build script for the mixr_ighost_cigi library.
#**
#*****************************************************************************

file(GLOB_RECURSE MIXR_IGHOST_CIGI_SOURCES "*.cpp")

add_library(mixr_ighost_cigi STATIC
  ${MIXR_IGHOST_CIGI_SOURCES}
)

target_include_directories(mixr_ighost_cigi PUBLIC
  ${CIGI_INCLUDE_DIRS}
)

target_link_libraries(mixr_ighost_cigi PUBLIC
  mixr_base
  mixr_models
  mixr_simulation
  ${CIGI_LIBRARIES}
)
