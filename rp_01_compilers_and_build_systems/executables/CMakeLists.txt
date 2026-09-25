# TODO: compile executable that will be run
add_executable(many_object_in_stack_example many_object_in_stack_example.cpp)
#add_executable(name source)

# TODO: link the executable against the core_library
target_link_libraries(many_object_in_stack_example core_library)
#core_library is given from add_library (in src/CMakeLists.txt)
#src is processed before executable