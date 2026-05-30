#********* Copyright © 2026 Jishnu Periya, Jonathon Bell. All rights reserved.
#**
#**  Purpose : CMake build script for the mixr_interop library.
#**
#*****************************************************************************

file(GLOB MIXR_INTEROP_SOURCES "*.cpp")

add_library(mixr_interop STATIC
  ${MIXR_INTEROP_SOURCES}
)

target_link_libraries(mixr_interop PUBLIC
  mixr_base
  mixr_models
  mixr_simulation
)

add_subdirectory(dis)

find_package(RTI QUIET)
if(RTI_FOUND)
  add_subdirectory(hla)
endif()
