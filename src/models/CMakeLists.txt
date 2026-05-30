#********* Copyright © 2026 Jishnu Periya, Jonathon Bell. All rights reserved.
#**
#**  Purpose : CMake build script for the mixr_models library.
#**
#*****************************************************************************

file(GLOB_RECURSE MIXR_MODELS_SOURCES "*.cpp")
list(FILTER MIXR_MODELS_SOURCES EXCLUDE REGEX ".*/dynamics/jsbsim/.*\\.cpp$")

add_library(mixr_models STATIC
  ${MIXR_MODELS_SOURCES}
)

target_link_libraries(mixr_models PUBLIC
  mixr_base
  mixr_simulation
  mixr_terrain
)

find_package(JSBSim QUIET)
if(JSBSim_FOUND)
  add_subdirectory(dynamics/jsbsim)
endif()
