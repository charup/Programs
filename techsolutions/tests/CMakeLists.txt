file(GLOB TESTS_SRC
   "*.h"
   "*.cc"
)
set(TESTS_SRC ${TESTS_SRC}
  ${PROJECT_SOURCE_DIR}/3rdparty/gtest/gtest-all.cc
  ${PROJECT_SOURCE_DIR}/3rdparty/gtest/gtest_main.cc
)

include_directories(${PROJECT_SOURCE_DIR}/src)
include_directories(${PROJECT_SOURCE_DIR}/3rdparty)

add_executable(tests ${TESTS_SRC})
target_link_libraries(tests techsolutions pthread)

