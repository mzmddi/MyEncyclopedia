# OpenGL Introduction

OpenGL = Open Graphics Library

For rendering 2D and 3D vector graphics by interacting directly with the machines GPU.

At it's core, OpenGL acts more like a state-machine managed by the gpu. You issue commands that change the OpenGL global state and issue draw calls that tells your GPU to draw whatever you are inputing in the draw call based on the current global state.

## Using OpenGL

(Only in the context of C++)

In order to use OpenGL, you must set up the environment so that your project is linked to the library through a Makefile.

## Setting up OpenGL in Docker

(In the context of c++)

In order to use OpenGL, you would need to set up the library in the correct environment. The easiest way to do this is with docker.

(In the context of Ubuntu:20.04)

Set up the container however you want, but here are the install lines necessary for OpenGL:

**libx11-dev**
X11 Window System Client Development Files  
Contains header files and libraries for communicaion with the Linux X Window System (I am on MacOS). GLFW requires this under the hood on Linus to create windows, receive OS events, and interface with the screen.

**libgl1-mesa-dev**  
Mesa OpenGL Development Headers & Libraries  
This provides the core headers and linking libraries implemented by Mesa. It exposes core rendering commands, and viewport operations.

**libglew-dev**  
OpenGL Extension Wrangler Library  
Handles modern OpenGL functions loading across different graphic drivers.

**libglfw3-dev**  
Graphics Library Framework 3  
Provides a modern API to create native OS windows, manage OpenGL rendering contexts, and handles user inputs (keyboard, mouse movements, etc).

**libglm-dev**  
OpenGL Mathematics  
Supplies matrix, vector, and quaternion data structures, along with transformation utilities. Designed to match the syntax and layout of GLSL (OpenGL Shading Language) variables.

## Setting up OpenGL in the CMakeLists

(Only in the context of C++)

In the CMakeLists.txt file, you need to call the libraries you installed, and link them to your executable.

**CMakeLists.txt**

```
find_package(OpenGL REQUIRED)
find_package(GLEW REQUIRED)
find_package(glfw3 REQUIRED)
find_package(glm REQUIRED)

target_link_libraries(test_opengl OpenGL::GL GLEW::GLEW glfw glm::glm)
```

## The 3 big library components

OpenGL is comprised of 3 big libraries working together.

- GLFW => Manages the operating system window, context, and keyboard/mouse inputs.
- GLEW => Queries your GPU driver at runtime to map pointers for modern OpenGL functions.
- GLM => The math part of OpenGL (matrix, matrix op, etc)

## The includes

**Ordering of the #include is important!**

```
#include <GL/glew.h>
// this has to be the first one

#include <GLFW/glfw3.h>
// this must be the second one

#include <glm/glm.hpp>
// Lastly, the math part.
```

## Fundamental Concepts when writing code

**VAO**  
Vertex Array Object  
A state container that stores how your vertex data is laid out and which buffers are bound.

**VBO**  
Vertex Buffer Object  
A chuink of memory allocated directly on the GPU VRAM that holds array data.

**Vertex Shader**
A GLSL script executed on the GPU once per vertex to transform the 3D world coordinates into screen coordinates.

**Fragment Shader**
A GLSL script executed on the GPU once per pixel to compute the final RGBA color. (the A is alpha).

## Sources

- [Wikipedia](https://en.wikipedia.org/wiki/OpenGL)
- [Wiki-Khronos](https://wikis.khronos.org/opengl/Getting_Started)
- [ogldev](https://ogldev.org/)
