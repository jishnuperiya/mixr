#********* Copyright © 2026 Jishnu Periya, Jonathon Bell. All rights reserved.
#**
#**  Purpose : CMake build script for ui sub-libraries.
#**
#*****************************************************************************

find_package(GLUT QUIET)
if(GLUT_FOUND)
  add_subdirectory(glut)
endif()
