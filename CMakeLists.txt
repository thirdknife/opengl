cmake_minimum_required(VERSION 3.25)
project(opengl)

set(CMAKE_CXX_STANDARD 20)

add_executable(opengl
        main.cpp
        imgui_impl_glfw.cpp
        imgui_impl_opengl3.cpp
        VAO.cpp
        VBO.cpp
        EBO.cpp
        shaderClass.cpp
)

find_package(imgui CONFIG REQUIRED)
target_link_libraries(opengl PRIVATE imgui::imgui)

find_package(glad CONFIG REQUIRED)
target_link_libraries(opengl PRIVATE glad::glad)

find_package(glfw3 CONFIG REQUIRED)
target_link_libraries(opengl PRIVATE glfw)

find_package(glm CONFIG REQUIRED)
target_link_libraries(opengl PRIVATE glm::glm)

find_package(assimp CONFIG REQUIRED)
target_link_libraries(opengl PRIVATE assimp::assimp)

