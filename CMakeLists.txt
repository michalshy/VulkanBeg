cmake_minimum_required(VERSION 3.16)
project(vulkanBeg)

set(CMAKE_CXX_STANDARD 17)
find_package(Vulkan REQUIRED)

add_subdirectory(lib/glfw-3.4 EXCLUDE_FROM_ALL)
add_subdirectory(lib/glm EXCLUDE_FROM_ALL)

add_executable(${PROJECT_NAME} main.cpp)

target_link_libraries(${PROJECT_NAME} PRIVATE Vulkan::Vulkan  
                        PRIVATE glfw
                        PRIVATE glm::glm)