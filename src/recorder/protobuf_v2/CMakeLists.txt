#********* Copyright © 2026 Jishnu Periya, Jonathon Bell. All rights reserved.
#**
#**  Purpose : CMake build script for the mixr_recorder_protobuf_v2 library.
#**
#*****************************************************************************

file(GLOB_RECURSE MIXR_RECORDER_SOURCES "*.cpp")

add_library(mixr_recorder_protobuf_v2 STATIC
  ${MIXR_RECORDER_SOURCES}
)

target_include_directories(mixr_recorder_protobuf_v2 PUBLIC
  ${Protobuf_INCLUDE_DIRS}
)

target_link_libraries(mixr_recorder_protobuf_v2 PUBLIC
  mixr_base
  mixr_models
  mixr_simulation
  ${Protobuf_LIBRARIES}
)
