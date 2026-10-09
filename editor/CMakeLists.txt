find_package(glfw3 REQUIRED)

add_executable(editor
    src/main.cpp
)

target_link_libraries(editor PRIVATE engine glfw glad)
