# Add executable
add_executable(example1 src/main.cpp)

# Link Engine library
target_link_libraries(example1 PRIVATE engine)

# Include directories for example1
target_include_directories(example1 PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/src)

# Compiler-specific options
if(CMAKE_CXX_COMPILER_ID MATCHES "GNU|Clang")
    target_compile_options(example1 PRIVATE -Wall -Wextra -Wpedantic)
endif()
