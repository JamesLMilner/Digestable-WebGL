# Digestable WebGL - Chapter 0.4: Points

## Drawing a Point

The time has come to actually draw something!

## The Rendering Pipeline

   1. Vertices in a Typed Array in JavaScript code
   2. Passed to Buffer Object in the WebGL system
   3. Pass vertices to Vertex Shader (attributes)
   4. Shape assembly -
   5. Rasterization - turn the shapes from vectors to rasters (fragments)
   6. Fragment Shader
   7. Color Buffer
   8. Rendered in Browser


## Shaders
As previously discussed shaders are responsible for helping us draw something in a specific way to the screen. In WebGL we have two types of shaders we need to draw something to the screen, namely a ***vertex shader*** and a ***fragment shader***.

### Vertex Shaders
A vertex shader has the job of determining the position and potentially the colours and size of the vertices on the screen that you pass to it. The vertex shader is responsible for setting builtin variables gl_Position, gl_PointSize.

### Fragment Shaders
Fragment shaders provide colour values to pixels on the canvas. Fragments can be thought of a special type of pixel that are produced after the rasterisation process. They have additional information for example position, depth, color that become available after the geometries have been assembled and rasterized. The fragment shader is responsible for setting gl_FragColour.

## GLSL

## Compiling a Shader

## Drawing a Line






## Credits and Sources

1. Nvidia - [What’s the Difference Between a CPU and a GPU?]( http://blogs.nvidia.com/blog/2009/12/16/whats-the-difference-between-a-cpu-and-a-gpu/)


## Image Credits

[Dolphin - Public Domain]](https://upload.wikimedia.org/wikipedia/commons/f/fb/Dolphin_triangle_mesh.png
