# The Flutter tooling requires that developers have CMake 3.10 or later
# installed. You should not increase this version, as doing so will cause
# the plugin to fail to compile for some customers of the plugin.
cmake_minimum_required(VERSION 3.10)

project(vivysub_libass_library VERSION 0.0.1 LANGUAGES C)

add_library(vivysub_libass SHARED
  "vivysub_libass.c"
)

set_target_properties(vivysub_libass PROPERTIES
  PUBLIC_HEADER vivysub_libass.h
  OUTPUT_NAME "vivysub_libass"
)

target_compile_definitions(vivysub_libass PUBLIC DART_SHARED_LIB)
