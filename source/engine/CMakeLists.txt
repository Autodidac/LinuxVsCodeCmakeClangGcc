# Add engine library
add_library(engine STATIC)

# Include directories
target_include_directories(engine PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/src)

# Source files for the engine
target_sources(engine PRIVATE
    ${CMAKE_CURRENT_SOURCE_DIR}/src/main.cpp  # Replace with actual sources
)

# Compiler-specific options
if(CMAKE_CXX_COMPILER_ID MATCHES "GNU|Clang")
    target_compile_options(engine PRIVATE -Wall -Wextra -Wpedantic)
endif()
