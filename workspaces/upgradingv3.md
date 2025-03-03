# Upgrading Engine Version

This guide walks you through moving your project from **Moddio v2** to **Moddio v3**, highlighting key steps, potential pitfalls, and new features to explore.
<div style="text-align: center; margin: 20px 0;">
  <img 
    src="Imgs/engineupgrade.PNG"
    style="width: 1200px; height: auto;" />
</div>

---

## Why Upgrade to v3?

1. **Enhanced 3D Support**  
   - **Server Physics Engine (Rapier3D)**: Full 3D physics simulation on the server.  
   - **Improved Rendering**: Expanded 3D rendering pipeline for more immersive visuals.

2. **Performance & Stability**  
   - Optimized engine tick rates and physics updates.  
   - Better handling of large or complex scenes.

3. **New Tools & Editor Improvements**  
   - Streamlined UI for configuring 3D settings, camera controls, and lighting.  
   - Future-ready architecture to support upcoming features.


---

## Step-by-Step Upgrade Instructions

1. **Backup Your Project**  
   - Export your v2 project or save a local copy.  
   - Keep a backup of any custom scripts, assets, or data to avoid accidental loss.

2. **Open Configuration**  
   - In the Moddio editor, go to **Configuration → Engine**.  
   - Locate the **Engine Version** dropdown.

3. **Select v3**  
   - Choose **3.x.x** (e.g., `3.0.2`) from the available versions.  
   - Confirm any prompts about migrating settings or assets.

4. **Review Physics & Rendering Settings**  
   - **Server Physics Engine**: If you plan to use 3D, select **Rapier3D**.  
   - **Client Physics Engine**: You can set this to **None** or keep a 2D engine if you prefer.  
   - **Shadow Quality, Fog, or 3D Camera**: Check the **Rendering/Camera** tab for new 3D options.

5. **Update Scripts & Assets**  
   - If you rely on any v2-specific APIs or 2D-only scripts, verify they are still compatible.  
   - Consider importing new 3D models or converting existing assets to take advantage of v3’s capabilities.

6. **Test Your Game**  
   - Play test your game before publishing.  
   - Look for errors or performance issues related to 3D features (e.g., collision detection, camera angles).

7. **Publish & Monitor**  
   - Once you’re confident in the new setup, publish your game on v3.  
   - Monitor performance and gather player feedback to fine-tune 3D settings.

---

## Potential Breaking Changes

- **Physics API Adjustments**: Some functions or callbacks may differ in v3, especially if you switch to 3D physics.  
- **Asset Pipeline**: 3D models require different handling compared to 2D sprites.  
- **UI & Editor Layout**: Certain menus or configuration options have been reorganized for clarity.

> **Tip**: Keep your v2 project backup until you’ve fully tested your v3 upgrade to avoid any irreversible changes.

---

## Exploring New v3 Features

- **Full 3D Worlds**: Build expansive environments, add 3D objects, and create dynamic scenes.  
- **Advanced Camera Controls**: Configure pitch, yaw, perspective/orthographic views, and custom camera logic.  
- **Refined Performance Tools**: Adjust the **Physics Frame Rate** and **Engine Tick Rate** to balance fidelity and speed.

---

## Additional Resources

- [Moddio v3 Release Notes](#)  
- [Moddio v3 Documentation](#)  
- [3D Rendering & Camera Guide](#)

If you have any questions or encounter issues, join our community forums or contact support for assistance. Happy building in **Moddio v3**!
