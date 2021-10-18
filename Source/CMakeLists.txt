#-------------------------------------------------------------------------------------------
# Copyright (c) 2020-2021, the VkCraft developers.
#
# SPDX-License-Identifier: MIT
#-------------------------------------------------------------------------------------------

#-------------------------------------------------------------------------------------------
# VkCraft
#-------------------------------------------------------------------------------------------
set(SOURCES
        src/main.cpp)

set(HEADERS
        )

foreach (item IN ITEMS ${SOURCES} ${HEADERS})
    get_filename_component(src_path "${item}" PATH)
    string(REPLACE "${CMAKE_CURRENT_SOURCE_DIR}" "" group_path "${src_path}")
    string(REPLACE ".." "\\" group_path "${group_path}")
    source_group("${group_path}" FILES "${item}")
endforeach ()

add_executable(VkCraft ${SOURCES} ${HEADERS})
target_link_libraries(VkCraft
        PRIVATE
        ProjectOptions
        ProjectWarnings
        CONAN_PKG::fmt
        CONAN_PKG::glfw
        CONAN_PKG::vulkan-headers
        CONAN_PKG::vulkan-memory-allocator
        CONAN_PKG::volk)
target_include_directories(
        VkCraft
        PRIVATE
        include)
