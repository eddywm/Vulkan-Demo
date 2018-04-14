cmake_minimum_required(VERSION 3.9)
project(VulKanDemo)

set(CMAKE_CXX_STANDARD 17)

include_directories($ENV{VULKAN_SDK}/include)

find_package(PkgConfig REQUIRED)

pkg_search_module(GLFW REQUIRED glfw3)

include_directories(${GLFW_INCLUDE_DIRS})


add_executable(VulKanDemo main.cpp)

target_link_libraries(VulKanDemo ${GLFW_STATIC_LIBRARIES})

