# OpenGL Physics & Rendering Demo

This project is a C++ application that demonstrates 3D rendering using **OpenGL**, **GLFW**, and **GLAD**, combined with physics simulation using **ODE (Open Dynamics Engine)** and model loading using **Assimp**. The application displays a rotating textured cube, a textured plane, and a 3D model, all under a first-person camera system.

# Features

- Real-time 3D rendering with OpenGL
- Physics simulation using ODE (gravity, rigid body motion)
- Model loading via Assimp (`.fbx` format)
- Camera system with first-person movement and mouse look
- Textured cubes and ground plane using GLSL shaders
- Lighting-ready shader architecture (can be extended)
- Integration of third-party libraries: GLFW, GLAD, GLM, Assimp, stb_image, ODE

# Project Structure

my_en/
├── OppenGL/
│ ├── main.cpp # Main rendering and logic loop
│ ├── Camera.h # Camera class (FPS-style movement)
│ ├── mesh.h, model.h # Mesh and Model classes for Assimp
│ ├── shader.h # Shader loader and wrapper
│ ├── Cube_vertex.glsl # Vertex shader for the cube
│ ├── Cube_fragment.glsl # Fragment shader for the cube
│ ├── modelVertex.glsl # Vertex shader for models
│ ├── modelFragment.glsl # Fragment shader for models
│ ├── define_std_image.cpp # STB image support
│ ├── stb_image.h # Image loading (textures)
│ └── opengl/ # Folder for textures and related assets
├── OppenGL.sln # Visual Studio solution
├── OppenGL.vcxproj # Visual Studio project file
├── OppenGL.vcxproj.filters # Project file filters
├── assimp-vc143-mt.dll # Assimp dynamic library
├── ode_double.dll # ODE physics engine DLL
├── .gitignore
└── .gitattributes


# Requirements

- C++17 or later
- OpenGL 3.3+
- CMake (optional if using Visual Studio)
- External dependencies (some included as DLLs, see below)

# Libraries Used

| Library      | Purpose                         |
|--------------|----------------------------------|
| GLFW         | Window/context/input management |
| GLAD         | OpenGL function loading         |
| GLM          | Mathematics (vectors, matrices) |
| Assimp       | Model importing (.fbx, .obj)    |
| ODE          | Physics engine                  |
| stb_image    | Texture image loading           |

# Build Instructions (Windows / Visual Studio)

1. Clone the repository.
2. Open the `OppenGL.sln` in Visual Studio.
3. Make sure the following DLLs are present in the same directory as the `.exe`:
   - `assimp-vc143-mt.dll`
   - `ode_double.dll`
4. Build and run the project.

**Note:** Ensure you have the required development dependencies installed for Assimp and ODE, or use the provided DLLs.

# Controls

- `W` / `A` / `S` / `D` – Move camera
- Mouse – Look around
- `ESC` – Exit the application

# Screenshots

![image](https://github.com/user-attachments/assets/3881bd08-5da3-468c-85f4-3d1e32323ac4)

![image](https://github.com/user-attachments/assets/364d082c-31a1-4eea-83ae-96027a0daadc)


# License

This project is provided for educational and demonstration purposes. Feel free to adapt or extend it.


# Credits

- [Assimp](https://www.assimp.org/)
- [ODE](https://www.ode.org/)
- [stb_image](https://github.com/nothings/stb)
- [LearnOpenGL](https://learnopengl.com) – Basis for shader/camera architecture
