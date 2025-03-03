# Engine Settings

Below are the core engine parameters that define how your game runs at a fundamental level. Reference the screenshot above to see how each setting appears in the user interface.

<div style="text-align: center; margin: 20px 0;">
  <img 
    src="Imgs/config2.PNG"
    style="width: 1200px; height: auto;" />
</div>



## Engine Version
Indicates the specific release of the engine you’re currently using.
- **Example:** `2.9.16`  
- Clicking **change logs** may show you patch notes or version history.

---

## Maximum Players
Sets the total number of players that can join your game simultaneously.
- **Example:** `32`

---

## Server Life Span
Defines how long the server remains active before automatically shutting down.
- **Example:** `5` **Hours**

---

## Server Physics Engine
Determines which physics library runs on the server side.
- **Example:** **PlanckJS**
- Other options might offer different performance or feature sets.

---

## Client Physics Engine
Chooses which physics library runs on the client side (in players’ browsers).
- **Example:** **Box2DWASM** (optimized 2D physics library compiled to WebAssembly)

---

## Continuous Physics
Toggles whether continuous physics calculations are used to prevent fast-moving objects from tunneling through walls or other colliders.
- **Yes/No** toggle

---

## Physics Frame Rate
Sets how many times per second the physics engine updates.
- **Example:** `15` (higher values increase accuracy but can also increase CPU usage)

---

## Gravity
Specifies the direction and strength of gravity in your game world.
- **x, y, z** fields (in the screenshot, all are `0`, effectively disabling gravity)

---

## Engine Tick Rate
Controls how frequently the overall game engine updates per second (separate from the physics frame rate).
- **Example:** `20`
