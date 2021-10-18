# VkCraft
[![Build Windows](https://img.shields.io/github/workflow/status/HyperionOrg/VkCraft/build-windows?style=flat&label=Build%20Windows&logo=github)](https://github.com/HyperionOrg/VkCraft/blob/main/.github/workflows/build-windows.yml)
[![Build Linux](https://img.shields.io/github/workflow/status/HyperionOrg/VkCraft/build-linux?style=flat&label=Build%20Linux&logo=github)](https://github.com/HyperionOrg/VkCraft/blob/main/.github/workflows/build-linux.yml)
[![License](https://img.shields.io/badge/license-MIT-yellow?style=flat)](https://github.com/HyperionOrg/VkCraft/blob/main/LICENSE)

This repository contains the source code of the VkCraft. <br />
Anyone is welcome to contribute or use the source of the VkCraft.

## Contents
- [Getting Started](#getting-started)
- [Dependencies](#dependencies)
- [Contributing](#contributing)
- [License](#license)

## Getting Started

### Prerequisites
In order to build the game, you will need the following things installed:
- CMake
- Conan
- Python
- Vulkan SDK

### Installation
The commands shown in this section are Linux specific.
If you want to install it on Windows, then you have to use the associated installer.

1. Download CMake
```shell
sudo apt install cmake
```

2. Download Python3
```shell
sudo apt install python3
```

3. Install Conan
```shell
pip3 install conan
```

4. Install the Vulkan SDK

### Building
1. Download the source code by using Git and cloning the repository, or downloading it as a zip.
```shell
git clone ttps://github.com/HyperionOrg/VkCraft
cd VkCraft
```

2. Create a folder in which the CMake project files will be generated in.
```shell
mkdir build
cd build
```

3. Configure the project by using the <code><a href="https://github.com/HyperionOrg/VkCraft/blob/main/CMakeLists.txt">CMakeLists.txt</a></code> inside of the root directory.
```shell
cmake .. -D CMAKE_BUILD_TYPE=Debug
```

4. Build the project using CMake
```shell
cmake --build .
```

5. Run the game to check if everything was built successfully.

## Dependencies
- [fmt](https://github.com/fmtlib/fmt/blob/master/LICENSE.rst) Copyright (c) MIT License, Victor Zverovich 2012-present
- [glfw](https://github.com/glfw/glfw/blob/master/LICENSE.md) Copyright (c) zlib License, Marcus Geelnard 2002-2006 & Camilla Löwy 2006-2019
- [Vulkan-Headers](https://github.com/KhronosGroup/Vulkan-Headers/blob/master/LICENSE.txt) Copyright (c) Apache License 2.0, The Khronos Group Inc. 2019-2021
- [VulkanMemoryAllocator](https://github.com/GPUOpen-LibrariesAndSDKs/VulkanMemoryAllocator/blob/master/LICENSE.txt) Copyright (c) MIT, Advanced Micro Devices 2017-2021
- [volk](https://github.com/zeux/volk/blob/master/LICENSE.md) Copyright (c) MIT, Arseny Kapoulkine 2018-2019

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.
Please make sure to update tests as appropriate.

## License
VkCraft is distributed under the [MIT](https://github.com/HyperionOrg/VkCraft/blob/main/LICENSE) license.
