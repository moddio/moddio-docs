# Rendering and Camera Settings

This page controls how your game is drawn to the screen and how the camera behaves. Below is a detailed breakdown of each option shown in the screenshot.
<div style="float: right; margin: 0 0 1em 1em;">
  <img 
    src="Imgs/config3.PNG"
    alt="Environment Screenshot"
    title="Environment Screenshot"
    style="width: auto; height: auto;" />
</div>


## NOTE: Rendering vs. Physics

When choosing **2D** vs. **3D** rendering, it’s important to remember that **rendering** (how the scene looks) differs from how **physics** (object interactions) are calculated:

- **2D Rendering + 2D Physics**  
  Most common setup in **Version 2** of the engine. Physics calculations remain in a 2D plane, making it easier to handle collisions, movement, and camera tracking for side-scrollers or top-down games.

- **3D Rendering + 2D/3D Physics**  
  Involves drawing objects in three dimensions. While the engine supports some 3D features, the physics system in **Version 2** is still largely designed around 2D interactions (with experimental support for 3D). This means true 3D physics (e.g., collisions on all three axes) may have limited functionality.

> **Tip:** If you plan to fully utilize 3D elements, be aware of the experimental nature of 3D rendering and physics in this engine version. You may want to consider upgrading to engine version 3.x before.


## Rendering

### Default Renderer
Choose the engine used to draw your game:
- **Phaser (2D)**: Ideal for 2D games, providing a robust and optimized 2D rendering pipeline.
- **ThreeJS (3D)**: Experimental 3D engine integration, allowing 3D models, scenes, and effects.

> **Note:** In the screenshot, both are shown as toggleable options, with **ThreeJS (3D)** labeled as an **Experimental feature**.

### Rendering Filter
Defines the overall aesthetic or pixel-scaling style of your game:
- **Smooth**: Applies smoothing to graphics, reducing pixelation.
- **Pixel Art**: Retains crisp, blocky pixels, often preferred for retro-style games.

### Shadow Quality
Determines how shadows appear in your game:
- **Simple**: Basic shadow rendering with minimal performance overhead.
- *(Other potential options may include “High,” “Medium,” or “None,” depending on your setup.)*

---

## Default Camera Settings

These settings determine the starting parameters and behavior of the in-game camera.

1. **Default Camera Zoom**  
   - Sets the initial zoom level for the camera.  
   - *Example:* `700` can be a moderate zoom-out, suitable for an overhead view.

2. **Default Camera Pitch**  
   - The vertical angle of the camera relative to the game world.  
   - *Example:* `90` degrees often indicates a top-down perspective in a 3D setting.

3. **Default Camera Yaw**  
   - The horizontal rotation of the camera.  
   - *Example:* `0` aligns the camera along a default axis.

4. **Camera Tracking Speed**  
   - How quickly the camera follows the player or target.  
   - *Example:* `3` indicates a moderate tracking speed.

5. **Map Bound Camera**  
   - Restricts the camera’s movement to stay within the boundaries of your map.  
   - Can be **Enabled** or **Disabled**.

6. **Set Camera Deadzone**  
   - Creates a “safe area” around the player before the camera begins to move.  
   - *Example:* **Yes** or **No** toggle to activate/deactivate this feature.

7. **Camera Collisions**  
   - Prevents the camera from clipping through walls or other obstacles in your game world.  
   - Can be **Enabled** or **Disabled**.

8. **Map Preview Position**  
   - Defines the camera’s center coordinates for the map’s initial preview.  
   - *Example:* `x center (px)` and `y center (px)` inputs.

---

<div style="float: right; margin: 0 0 1em 1em;">
  <img 
    src="Imgs/config33.PNG"
    alt="Environment Screenshot"
    title="Environment Screenshot"
    style="width: auto; height: auto;" />
</div>






## Additional 3D Settings

### Camera Projection Mode
Choose how your 3D scene is projected:
- **Orthographic**: Objects maintain the same size, regardless of distance from the camera. Useful for certain stylized or isometric views.  
- **Perspective**: Objects appear smaller as they get farther away, mimicking the way our eyes perceive distance.

### Skybox
Allows you to set a surrounding “box” of images to create the illusion of a distant horizon or environment:
- **Up, Down, Left, Right, Front, Back**: Six separate images that make up the skybox.  
- Click **Upload** to add your images for each face.

---
<div style="float: right; margin: 0 0 1em 1em;">
  <img 
    src="Imgs/config333.PNG"
    alt="Environment Screenshot"
    title="Environment Screenshot"
    style="width: auto; height: auto;" />
</div>

<div style="float: right; margin: 0 0 1em 1em;">
  <img 
    src="Imgs/config3333.PNG"
    alt="Environment Screenshot"
    title="Environment Screenshot"
    style="width: auto; height: auto;" />
</div>

## Environment

### Fog
Creates atmospheric depth by reducing visibility over distance:
- **Enabled/Disabled**: Toggles whether fog is active.
- **Color**: The color of the fog (e.g., `#fff` for white).
- **Intensity**: How dense or “thick” the fog appears.

### Ambient Light
Represents a global, directionless light in the scene:
- **Color**: Sets the hue of the ambient light (e.g., `#fff` for white).
- **Intensity**: Brightness of the ambient light.

### Directional Light
A directional light acts like the sun, shining from a specific direction:
- **Position (x, y, z)**: The light’s origin in 3D space.
- **Color**: Color of the directional light (e.g., `#fff`).
- **Intensity**: How strong or bright the light appears.

---


## Water

This section controls how water is rendered in your game, from tile placement to shader properties.

### Tile IDs
- **Top Left Corner, Top Right Corner, Down Left Corner, etc.**: Lists of tile IDs (e.g., “10,15”) indicating which tiles in your map should be rendered as water corners or edges.

### Water Color & Opacity
- **WaterColor**: Base color of the water (e.g., `#5fa0c3`).
- **waterOpacity**: How transparent or opaque the water appears.

### Caustics
- **CausticColor / causticOpacity**: Color and visibility of underwater light patterns.  
- **CausticHighlightColor / causticHighlightOpacity**: Additional highlights for brighter, refracted areas.

### Noise & Movement
- **NoiseScale**: Controls the scale of the noise texture used on the water surface.  
- **NoiseModulateSpeed** and **NoiseStrength**: Adjust how fast and how intense the noise distortions are.  
- **SpecularNoiseMovementStrength** and **SpecularSpeed**: Tweak the water’s reflective highlights and how quickly they move.

### Caustic Texture & Movement
- **CausticTextureScale**: Changes the size of the caustic pattern.  
- **CausticMovementScale** and **CausticMovementSpeed**: How much and how quickly the caustic pattern shifts over time.  
- **CausticMovementStrength**: The intensity or amplitude of caustic motion.

### Foam & Waves
- **FoamNoiseScale** and **FoamNoiseAmount**: Control how foam is generated on the water surface.  
- **FoamFrequency** and **FoamQuantizeAmount**: Adjust the pattern and distribution of foam.  
- **WaveSpeed**: Determines how fast the water waves move.