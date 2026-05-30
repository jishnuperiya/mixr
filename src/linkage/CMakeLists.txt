#********* Copyright © 2026 Jishnu Periya, Jonathon Bell. All rights reserved.
#**
#**  Purpose : CMake build script for the mixr_linkage library.
#**
#*****************************************************************************

file(GLOB_RECURSE MIXR_LINKAGE_SOURCES "*.cpp")

if(WIN32)
  list(FILTER MIXR_LINKAGE_SOURCES EXCLUDE REGEX ".*_linux\\.cpp$")
else()
  list(FILTER MIXR_LINKAGE_SOURCES EXCLUDE REGEX ".*_msvc\\.cpp$")
  list(FILTER MIXR_LINKAGE_SOURCES EXCLUDE REGEX ".*_mingw\\.cpp$")
endif()

add_library(mixr_linkage STATIC
  ${MIXR_LINKAGE_SOURCES}
)

target_link_libraries(mixr_linkage PUBLIC
  mixr_base
)
