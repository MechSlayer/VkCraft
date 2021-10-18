#-------------------------------------------------------------------------------------------
# Copyright (c) 2020-2021, the VkCraft developers.
#
# SPDX-License-Identifier: MIT
#-------------------------------------------------------------------------------------------

#-------------------------------------------------------------------------------------------
# CMake Info
#-------------------------------------------------------------------------------------------
cmake_minimum_required(VERSION 3.15)
project(VkCraft LANGUAGES C CXX)

#-------------------------------------------------------------------------------------------
# Modules
#-------------------------------------------------------------------------------------------
include(Development/CMake/StandardProjectSettings.cmake)

#-------------------------------------------------------------------------------------------
# Project Libraries
#-------------------------------------------------------------------------------------------
add_library(ProjectOptions INTERFACE)
target_compile_features(ProjectOptions INTERFACE cxx_std_17)

add_library(ProjectWarnings INTERFACE)

#-------------------------------------------------------------------------------------------
# Standard Settings
#-------------------------------------------------------------------------------------------
include(Development/CMake/Cache.cmake)

include(Development/CMake/CompilerWarnings.cmake)
enable_warnings(ProjectWarnings)

include(Development/CMake/Sanitizers.cmake)
enable_sanitizers(ProjectOptions)

include(Development/CMake/Doxygen.cmake)
enable_doxygen()

include(Development/CMake/StaticAnalyzers.cmake)

#-------------------------------------------------------------------------------------------
# Conan
#-------------------------------------------------------------------------------------------
set(CONAN_LIBRARIES
        fmt/8.0.1
        glfw/3.3.4
        vulkan-headers/1.2.190
        vulkan-memory-allocator/2.3.0
        volk/1.2.190)

include(Development/CMake/Conan.cmake)
run_conan()

#-------------------------------------------------------------------------------------------
# Source
#-------------------------------------------------------------------------------------------
add_subdirectory(Source)
