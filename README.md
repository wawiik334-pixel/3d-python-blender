Here is the updated, simplified README.md for your Blender project, reflecting the "simple" setup where bark.jpg is expected to be in the same folder as the script.

Procedural World Generation and Animation
A Python-based automation utility for Blender 4.5 that generates a complete 3D environment via script. The project features a recursively generated fractal structure, a noise-based terrain system with water-level detection, and a procedural forest generation system.

Features
Recursive Fractal Geometry: Implements a recursive subdivision algorithm to construct a complex 3D pyramid structure from primitive cylinders.

Noise-Driven Landscape: Generates terrain using multi-octave noise functions, including automated vertex coloring based on elevation and slope.

Environmental Constraints: Features a lookup system that utilizes coordinate snapping to ensure procedural trees are only placed on valid terrain (above water level).

Automated Animation: Utilizes scripted drivers and keyframing to simulate a sun cycle and constant rotational showcase of the central fractal.

Zero-Asset Dependency: Aside from a single bark texture, the entire scene (geometry, lighting, and animation) is constructed entirely from code.

Technical Implementation
bpy & bmesh API: Advanced use of Blender's low-level bmesh module for high-performance mesh editing and vertex color layer management.

Vector Mathematics: Utilizes mathutils for cross-product calculations, quaternion rotations, and spatial positioning of branching tree segments.

Memory Management: Implements scene cleanup logic to flush data blocks and ensure a clean environment upon script execution.

Linear Interpolation: Used for color blending and terrain gradients to create stylized environmental transitions without high-resolution textures.

Project Structure
src/: Contains the primary Python generation script (generate_scene.py) and the required bark.jpg texture.

docs/: Includes rendered samples and demonstration media of the generated output.

Getting Started
Prerequisites
Blender 4.5.

Important: The bark.jpg file must be located in the same directory as the .py script for the tree materials to load correctly.

Execution
Open Blender.

In the Scripting workspace, open src/generate_scene.py.

Press Run Script.

Note: The script is designed to run in a default empty scene and will automatically configure the viewport to Rendered mode upon completion.
