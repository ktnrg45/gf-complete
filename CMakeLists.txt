
cmake_minimum_required(VERSION 3.0.0)
project(gf_complete VERSION 1.0.0)

include(CTest)
enable_testing()


set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)

set(SRCS
  src/gf.c
  src/gf_cpu.c
  src/gf_general.c
  src/gf_method.c
  src/gf_rand.c
  src/gf_w128.c
  src/gf_w16.c
  src/gf_w32.c
  src/gf_w4.c
  src/gf_w64.c
  src/gf_w8.c
  src/gf_wgen.c
  )

# set(NEON_SRCS
#   src/neon/gf_w16_neon.c
#   src/neon/gf_w32_neon.c
#   src/neon/gf_w4_neon.c
#   src/neon/gf_w64_neon.c
#   src/neon/gf_w8_neon.c
#   )

set(HEADERS
  include/gf_complete.h
  include/gf_method.h
  include/gf_rand.h
  include/gf_general.h
  )

include_directories(include)
add_library(gf_complete ${SRCS} ${HEADERS})
