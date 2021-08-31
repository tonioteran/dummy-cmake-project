cmake_minimum_required(VERSION 3.10)
project(dummy)

# Create library.
add_library(dummy-lib SHARED src/dummy.cc)
target_include_directories(dummy-lib PUBLIC include)

# Make library reachable by other cmake projects.
export(PACKAGE dummy-lib)
export(TARGETS dummy-lib FILE dummy-libConfig.cmake)
