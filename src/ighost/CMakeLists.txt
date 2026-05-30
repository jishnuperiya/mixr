#********* Copyright © 2026 Jishnu Periya, Jonathon Bell. All rights reserved.
#**
#**  Purpose : CMake build script for ighost sub-libraries.
#**
#*****************************************************************************

add_subdirectory(flightgear)
add_subdirectory(pov)

find_package(CIGI QUIET)
if(CIGI_FOUND)
  add_subdirectory(cigi)
endif()
