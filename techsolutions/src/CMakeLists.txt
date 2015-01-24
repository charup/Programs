# include all source files
file(GLOB_RECURSE TECHSOLUTIONS_SRC .
   "*.h"
   "*.cc"
)

add_library(techsolutions ${TECHSOLUTIONS_SRC})

install (TARGETS techsolutions DESTINATION lib)
install (DIRECTORY . DESTINATION include
  FILES_MATCHING PATTERN "*.h")

