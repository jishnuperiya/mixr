#********* Copyright © 2026 Jishnu Periya, Jonathon Bell. All rights reserved.
#**
#**  Purpose : CMake build script for the mixr_ui_glut library.
#**
#*****************************************************************************

file(GLOB_RECURSE MIXR_UI_GLUT_SOURCES "*.cpp")

add_library(mixr_ui_glut STATIC
  ${MIXR_UI_GLUT_SOURCES}
)

target_link_libraries(mixr_ui_glut PUBLIC
  mixr_base
  GLUT::GLUT
)
