
add_executable(app main.cpp)
add_dependencies(app SFML_lib)
target_link_libraries(app PRIVATE SFML_lib)