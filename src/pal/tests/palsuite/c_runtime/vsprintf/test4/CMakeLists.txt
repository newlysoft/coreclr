cmake_minimum_required(VERSION 2.8.12.2)

set(CMAKE_INCLUDE_CURRENT_DIR ON)

set(SOURCES
  test4.c
)

add_executable(paltest_vsprintf_test4
  ${SOURCES}
)

add_dependencies(paltest_vsprintf_test4 CoreClrPal)

target_link_libraries(paltest_vsprintf_test4
  pthread
  rt
  m
  CoreClrPal
)
