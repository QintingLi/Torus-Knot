# Three.js Custom Shader Example

This project demonstrates a basic implementation of a custom shader using Three.js, a popular JavaScript library for 3D graphics. The example uses a custom fragment and vertex shader to create a hatching effect on a 3D object (a Torus Knot), and allows the user to interact with the 3D scene using orbit controls.

## Table of Contents
- [Background](#background)
- [Features](#features)
- [Requirements](#requirements)
- [Usage](#usage)
- [Code Explanation](#code-explanation)
- [License](#license)

## Background

Shaders are powerful tools in graphics programming that allow developers to create custom visual effects by manipulating the GPU's rendering pipeline. This project uses Three.js to create a custom shader that applies a hatching effect to a 3D object. The scene is rendered in real-time and allows user interaction with orbit controls.

## Features

- **Custom Shaders**: Uses GLSL to create a custom fragment shader for hatching effect.
- **Interactive 3D Scene**: Provides orbit controls for rotating and zooming in the 3D scene.
- **Dynamic Lighting**: Includes a directional light source that moves dynamically to create varying lighting effects.
- **3D Object**: Renders a Torus Knot geometry with the custom shader material.

## Requirements

To run this project, you need a modern web browser with WebGL support. Additionally, make sure to have an internet connection to load the Three.js library from the CDN.

### Files Needed
- `three.min.js`: Three.js library for rendering 3D graphics.
- `OrbitControls.min.js`: Three.js orbit controls for enabling user interaction.

## Usage

1. **Clone or download the repository**:
   ```bash
   git clone https://github.com/yourusername/threejs-custom-shader-example.git
   ```

2. **Open the HTML file in your browser**:
   - Navigate to the directory where the project files are located.
   - Open `index.html` in a modern web browser.

3. **Interact with the 3D scene**:
   - Use your mouse to rotate, zoom, and pan around the Torus Knot geometry.

## Code Explanation

- **Scene Setup**: Creates a Three.js scene with a black background and a perspective camera.
- **Renderer**: Sets up a WebGL renderer to draw the scene and attaches it to the HTML document.
- **Orbit Controls**: Adds orbit controls to allow the user to interact with the scene using the mouse.
- **Lighting**: A directional light source is added to the scene to illuminate the object and create shadows.
- **Custom Shader Material**:
  - **Uniforms**: Defines several uniforms for light position, color, and the base and line colors for the hatching effect.
  - **Vertex Shader**: A simple shader that passes the normal vector to the fragment shader.
  - **Fragment Shader**: Applies a hatching effect based on the light intensity and fragment coordinates.
- **Geometry and Mesh**: Creates a Torus Knot geometry and applies the custom shader material.
- **Animation Loop**: Uses `requestAnimationFrame` to continuously render the scene and update the light position dynamically to create an animated effect.

