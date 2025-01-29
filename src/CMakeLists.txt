include(SFML)
include(CMakePrintHelpers)

# print sfml-system properties
cmake_print_properties(TARGETS sfml-system
        PROPERTIES TYPE SOURCE_DIR
)

# Wrap SFML components into a single lib
add_library(SFML_lib INTERFACE)
target_link_libraries(SFML_lib INTERFACE sfml-system sfml-graphics sfml-window sfml-audio sfml-network)

add_subdirectory(app)
