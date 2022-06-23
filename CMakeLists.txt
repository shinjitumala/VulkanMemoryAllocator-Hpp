cmake_minimum_required(VERSION 3.16)

project(vma-hpp DESCRIPTION "C++ binding for VulkanMemoryAllocator.")

find_package(VulkanMemoryAllocator REQUIRED CONFIG)

add_library(vma-hpp INTERFACE)
target_link_libraries(vma-hpp INTERFACE VulkanMemoryAllocator)
target_include_directories(vma-hpp INTERFACE include)

export(TARGETS vma-hpp FILE ${CMAKE_CURRENT_BINARY_DIR}/vma-hppConfig.cmake)
