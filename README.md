# Godot crt-lottes shader
This is a port of the libretro crt-lottes GLSL shader to Godot shading language.

The original source is: https://github.com/libretro/glsl-shaders/blob/master/crt/shaders/crt-lottes.glsl

There is a basic example scene, consisting in just a `ViewportContainer`, with a `Viewport` containing a "game" scene.
The `ViewportContainer` has the shader asigned to its `material` property, and must be upscaled using the `rect_scale` property, preferably using an integer factor (x2, x3, x4...).

In the shader params must specify:
 - `input size`: resolution of source image. In this example, 256x224.
 - `output size`: resolution of final image. In this example it is scaled x4, so it is 1024x896.
 - `texture size`: must be equal to `input size`.

In project settings, disable any window stretching mode.

The original Lottes shader was made by Timothy Lottes and is public domain, and this port is also.
