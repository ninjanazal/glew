CMAKE_MINIMUM_REQUIRED( VERSION 3.26)
PROJECT(glew)


# Add the GLEW library
add_library(glew STATIC
    src/glew.c
)

target_include_directories(glew PRIVATE src/ include/)
target_include_directories(glew PUBLIC 
    ${PROJECT_SOURCE_DIR}/include/
)

target_compile_definitions(glew PUBLIC GLEW_STATIC )