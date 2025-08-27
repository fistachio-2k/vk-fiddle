### Fiddling with Vk

[![Nightly](https://github.com/fistachio-2k/vk-fiddle/actions/workflows/nightly-build.yml/badge.svg)](https://github.com/fistachio-2k/vk-fiddle/actions/workflows/nightly-build.yml)
[![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20Linux-lightgrey.svg)](#)
[![C++](https://img.shields.io/badge/C%2B%2B-20-blue.svg)](#)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE.txt)

This repo contains the progress of my first learning experience of Vulkan graphics API. I'm following https://vkguide.dev/ guide, while documenting my progress along the way.

#### Libraries Used

This project uses several libraries to simplify Vulkan development and provide essential functionality:

| Library | Type | Description |
|---------|------|-------------|
| **GLM** (OpenGL Mathematics) | Header-only | Mathematics library providing matrix and vector math functionality. Types are directly compatible with GLSL shader types (e.g., `glm::mat4` ↔ `mat4`). Despite the OpenGL name, works excellently with Vulkan. |
| **SDL** | Separately built | Cross-platform windowing and input library used by major engines (Unreal, Unity, Source). Provides easy window creation and detailed keyboard input handling across almost every platform. |
| **dear IMGUI** | Header-only | Immediate mode GUI library for creating interactive widgets like sliders and debug windows. Widely used in the game industry for debug tools and development interfaces. |
| **STB Image** | Header-only | Small, easy-to-use image loading library supporting common formats (BMP, PNG, JPEG, etc.). Part of the STB collection of single-file libraries. |
| **Tiny Obj Loader** | Header-only | Fast and lightweight library for loading .obj 3D model files. Simple solution for importing 3D geometry data. |
| **Vk Bootstrap** | Library | Abstracts Vulkan initialization boilerplate code that's typically written once and never modified. Simplifies instance creation, swapchain setup, and extension loading. Will be removed in optional chapters covering manual Vulkan setup. |
| **VMA** (Vulkan Memory Allocator) | Header-only | Implements safe and performant memory allocation for Vulkan buffers, images, and resources. Handles the complex task of Vulkan memory management that would otherwise require custom allocator implementation. |

#### How to Build

**Prerequisites:** Vulkan SDK, CMake 3.8+, C++20 compiler

```bash
# Generate the project
mkdir build && cd build
cmake ..

# Build the project
cmake --build . --config Release
```

The executable will be in the `bin/` directory.

#### Nightly Builds

Automated nightly builds are available for Windows and Linux platforms in both Debug and Release configurations. These builds are triggered daily at 2 AM UTC and on every push to the main branch.

- **Download:** Check the [Actions](../../actions) page for the latest build artifacts
- **Build Status:** See the badge above for current build status
- **Artifacts:** Each successful build stores compiled executables and shaders for 30 days

The nightly builds include:
- Compiled executable (`engine`)
- Compiled shaders (`.spv` files)
- All necessary runtime dependencies

#### Current Progress

**27.8** -
Opened black SDL window + printing key strokes with `Wow, you just pressed the V key!` message.