# WebGL Lighting Lab

## Overview

This lab introduces the fundamental concepts of lighting in computer graphics using WebGL. Students will explore how lighting calculations affect the appearance of a 3D object by modifying shaders and JavaScript code.

The lab begins with a working rotating cube and guides students through a series of lighting experiments involving:

- Ambient Lighting
- Diffuse Lighting
- Light Direction
- Colored Lighting
- Animated Lighting

Students will gain hands-on experience with shader programming and learn how modern graphics engines simulate light.

---

## Learning Objectives

By the end of this lab, students will be able to:

- Explain the purpose of lighting in 3D graphics.
- Describe the difference between ambient and diffuse lighting.
- Modify GLSL shaders.
- Change light direction using JavaScript uniforms.
- Create colored light sources.
- Animate a light source around a 3D object.
- Understand the role of surface normals in lighting calculations.

---

## Project Structure

```text
WebGLLightingLab/
│
├── lighting.html
├── lighting.js
├── vertexShader.glsl
├── fragmentShader.glsl
│
└── Common/
```
 
# Questions/Reflection
## Part 1: Examine the Fragment Shader
1. Ambient light gives a natural bit of light to the scene, akin to how the sun lights up floors/ceilings/etc even if the scene is faced away from any light sources.
2. Things would be singular colors/hard transitions & be black.
## Part 2: Ambient Lighting Experiments
1. The cube's shadows become pure black.
2. The shadows appear again & the cube is VERY bright white.
3. The entire cube is completely white, no more shadows.
## Part 3: Light Direction
### Experiment A
The closest side [from the start of the rotation] of the visible facing sides is bright, the rest are shadow.
### Experiment B
The farthest side is lit up, the rest is dark.
### Experiment C
The entire thing is shadowed now, though the top or bottom may be lit.
### Experiment D
Once again the entire thing is shadow, though presumably the top or bottom face is lit.
## Part 4: Colored Lighting
1. The red multiplier gets mulitplied by the diffuse, being 0, & thus, vanishes, leaving the ambient term & shadows untouched.
2. Yellow seems the brightest against the shadow, but magenta & green also creates a strong visual contrast.
## Part 5: Animated Light Source
1. The lights appear to move as the cube rotates.
2. The bright patches shift because the shadow's light direction rotates as well.
### Activity 5B: Animated Light Color
1. The highlights go through random rgb & shift color.
2. For the same reason as before, the lights shift as the light direction rotates.
### Activity 5C: Disco Cube
Same as above.
## Part 6: Day and Night Effect
1. The colorful-light parts are very bright while the shadows become very dark [black].

# Reflection
1. Natural light in a scene that, irl, would already be there regardless of a main light source
What is diffuse lighting?
2. 
Why do we need normal vectors?
What role does the dot product play in lighting calculations?
How does changing light direction affect a 3D object?
How does changing light color affect realism?
Which modification produced the most interesting result?
Why do game engines automate lighting calculations?