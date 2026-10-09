cmake_minimum_required(VERSION 3.20)

project(ShaderEngine
    VERSION 0.1.0
    LANGUAGES C CXX
)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

add_subdirectory(engine)
add_subdirectory(editor)

add_library(glad STATIC
    external/glad/src/glad.c
)
target_include_directories(glad PUBLIC
    external/glad/include
)

enable_testing()
add_subdirectory(tests)
