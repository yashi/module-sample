cmake_minimum_required(VERSION 3.20)
project(sample)

add_library(sample)
target_compile_options(sample PRIVATE -Wall -Wextra)
set_target_properties(sample PROPERTIES C_STANDARD 11)

target_include_directories(sample PUBLIC include)
add_subdirectory(src)

file(CONFIGURE OUTPUT .gitignore
  NEWLINE_STYLE UNIX
  CONTENT "*")
