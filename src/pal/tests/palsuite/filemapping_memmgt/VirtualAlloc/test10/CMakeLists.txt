cmake_minimum_required(VERSION 2.8.12.2)

set(CMAKE_INCLUDE_CURRENT_DIR ON)

set(SOURCES
  VirtualAlloc.c
)

add_executable(paltest_virtualalloc_test10
  ${SOURCES}
)

add_dependencies(paltest_virtualalloc_test10 CoreClrPal)

target_link_libraries(paltest_virtualalloc_test10
  pthread
  rt
  m
  CoreClrPal
)
