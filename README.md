### Fiddling with Vk
This repo contains the progress of my first learning experience of Vulkan graphics API. I'm following https://vkguide.dev/ guide, while documenting my progress along the way.

#### Libraries Used

This project uses several libraries to simplify Vulkan development and provide essential functionality:

| Library | Type | Description |
|---------|------|-------------|
| **GLM** (OpenGL Mathematics) | Header-only | Mathematics library providing matrix and vector math functionality. Types are directly compatible with GLSL shader types (e.g., `glm::mat4` ↔ `mat4`). Despite the OpenGL name, works excellently with Vulkan. |
| **GLFW** | Separately built | Lightweight, cross-platform windowing and input library specifically designed for OpenGL, Vulkan, and other graphics APIs. Provides simple window creation, input handling, and context management with minimal overhead. |
| **dear IMGUI** | Header-only | Immediate mode GUI library for creating interactive widgets like sliders and debug windows. Widely used in the game industry for debug tools and development interfaces. |
| **STB Image** | Header-only | Small, easy-to-use image loading library supporting common formats (BMP, PNG, JPEG, etc.). Part of the STB collection of single-file libraries. |
| **Tiny Obj Loader** | Header-only | Fast and lightweight library for loading .obj 3D model files. Simple solution for importing 3D geometry data. |
| **Vk Bootstrap** | Library | Abstracts Vulkan initialization boilerplate code that's typically written once and never modified. Simplifies instance creation, swapchain setup, and extension loading. Will be removed in optional chapters covering manual Vulkan setup. |
| **VMA** (Vulkan Memory Allocator) | Header-only | Implements safe and performant memory allocation for Vulkan buffers, images, and resources. Handles the complex task of Vulkan memory management that would otherwise require custom allocator implementation. |

#### Current Progress

