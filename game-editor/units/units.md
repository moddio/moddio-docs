# Units in Moddio

<div style="float: right; margin: 0 0 1em 1em;">
  <img 
    src="Imgs/unit.PNG"
    alt="Units Panel Screenshot"
    title="Units Panel Screenshot"
    style="width: 600px; height: auto;" />
</div>

Units in **Moddio** are **active entities** that represent **players, NPCs, and creatures** capable of **moving, interacting, and performing actions**. Unlike static entities like **items or projectiles**, Units have **health, AI, states, animations, and inventory**.

---

## What is a Unit?

A **Unit** is a specialized **Entity** that actively participates in **gameplay**. They can:
- **Move** (controlled by a player or AI)
- **Attack** (melee or ranged combat)
- **Interact with Objects** (picking up items, opening doors)
- **Have AI Behavior** (chasing, patrolling)
- **Hold Inventory** (weapons, potions)
- **Trigger Events** (on attack, on death, on idle)

> **Example:**  
> A **player-controlled character** that moves with WASD and attacks enemies is a **Unit**.  
> A **static tree** in the game world is an **Entity**, but **not a Unit**.

---

## Entities vs. Units

In **Moddio**, an **Entity** is **any object** in the game world, including:
- **Items** (weapons, potions, coins)
- **Projectiles** (arrows, fireballs)
- **Props** (barrels, rocks, trees)
- **Units** (players, NPCs, enemies)

> **All Units are Entities, but not all Entities are Units.**

🔹 **Example Difference:**
- A **rock** is an Entity but **not a Unit** because it doesn't move.
- A **player character** is a Unit because it has **movement, health, and AI**.

By specifying **"when a Unit’s attribute becomes 0 or less,"** we ensure the game only checks for **Units**, **not static objects like rocks or items**. This improves performance and simplifies scripting.

---

## Viewing & Managing Units

To **view and manage units**, navigate to the **Units panel**.

<div style="text-align: center;">
  <img 
    src="Imgs/unit1.PNG"
    alt="Units Panel"
    title="Units Panel"
    style="width: 600px; height: auto;" />
</div>

The **Units Panel** allows you to:
- **Create New Units**
- **Organize Units into Folders**
- **Edit and Customize Units**
- **Delete Unnecessary Units**

---

## Creating a New Unit

To **create a Unit**, follow these steps:
1. Click the **"New"** button.
2. Select **"Unit"** from the dropdown.
3. Choose from **predefined templates**:
   - **Top-down Unit** (rotates to mouse)
   - **Platformer Unit** (sprite flips)
   - **Collider Object** (static but has collision)

<div style="text-align: center;">
  <img 
    src="Imgs/unit2.PNG"
    alt="Unit Creation Panel"
    title="Unit Creation Panel"
    style="width: 12000px; height: auto;" />
</div>

---

## Unit Properties & Customization

Each Unit has multiple customizable properties, accessible through the **Unit Editor**.

### General Properties

| Property       | Description |
|---------------|-------------|
| **Name**      | The unit’s name (e.g., "Survivor"). |
| **States**    | Active effects like **stunned, burning, poisoned**. |
| **Attributes** | Stats like **health (HP), speed, stamina**. |
| **Animations** | Idle, walk, attack, death animations. |
| **Inventory** | Items the unit can carry. |

<div style="text-align: center;">
  <img 
    src="Imgs/unit3.PNG"
    alt="Unit Editor"
    title="Unit Editor"
    style="width: 12000px; height: auto;" />
</div>

---

## Unit Controls

The **Controls tab** lets you set up movement, keybindings, and behaviors.

### Movement & Keybindings

| Setting | Description |
|---------|-------------|
| **Movement Method** | Determines movement style (e.g., WASD or arrow keys). |
| **Rotate to Face Mouse** | Unit rotates towards the cursor. |
| **Keybindings** | Assign actions to keys (e.g., "E" for interacting). |

<div style="text-align: center;">
  <img 
    src="Imgs/unit4.PNG"
    alt="Unit Controls"
    title="Unit Controls"
    style="width: 12000px; height: auto;" />
</div>

---

## AI & Automation

Units can be **AI-controlled** with behaviors like:
- **Attacking enemies**
- **Chasing or fleeing from threats**
- **Patrolling predefined paths**

### AI Settings

| Setting | Description |
|---------|-------------|
| **Enable AI** | Determines if the unit uses AI behaviors. |
| **Attack Response** | Reacts to hostile units (e.g., attacks back). |
| **Max Attack Range** | Defines the range within which the unit attacks. |
| **Pathfinding** | Determines how the unit moves towards targets. |

<div style="text-align: center;">
  <img 
    src="Imgs/unit5.PNG"
    alt="Unit AI Settings"
    title="Unit AI Settings"
    style="width: 12000px; height: auto;" />
</div>

---

## Unit Effects & Interactions

Units can trigger **animations, sounds, and scripts** based on **specific events**.

### Event Triggers

| Trigger | Description |
|---------|-------------|
| **OnAttacked** | Plays an animation or sound when hit. |
| **OnCreate** | Runs a script when the unit spawns. |
| **OnDestroy** | Runs a script when the unit dies. |
| **OnIdle** | Defines what the unit does when not moving. |

<div style="text-align: center;">
  <img 
    src="Imgs/unit6.PNG"
    alt="Unit Events"
    title="Unit Events"
    style="width: 12000px; height: auto;" />
</div>

---

## Camera & Visibility

The **Camera tab** lets you configure:
- **Camera Lock** (whether the unit controls the camera)
- **Offset Adjustments** (adjust camera positioning)

The **Extra tab** contains **advanced settings** like:
- **Untargetable Mode** (hides from attacks)
- **Visibility Range** (controls unit visibility on the screen)

<div style="text-align: center;">
  <img 
    src="Imgs/unit7.PNG"
    alt="Unit Camera Settings"
    title="Unit Camera Settings"
    style="width: 12000px; height: auto;" />
</div>

---

## Example Use Cases for Units

### **Player Character**
- **Attributes:** Health = 100, Speed = 10
- **Controls:** WASD movement, left-click to attack
- **AI:** Disabled (player-controlled)
- **Inventory:** Starts with an Axe

### **Enemy NPC (Zombie)**
- **Attributes:** Health = 50, Speed = 5
- **AI:** Enabled (chases players)
- **Attack Response:** Attacks when close
- **Pathfinding:** Simple AI movement

### **Merchant NPC**
- **Attributes:** No attack or AI
- **Dialogue:** Opens a **shop** when interacted with
- **Inventory:** Holds a list of items to sell

---

## Summary

- **Units** are the primary **interactive and moving** entities in your game.
- They can have **attributes, states, AI, inventory, and animations**.
- Units are a **subset of Entities**—while all **Units are Entities, not all Entities are Units**.
- Units can be **controlled by players or AI**.
- They can be **customized with effects, events, and interactions**.

With **Units**, you can **build dynamic gameplay**, including **players, NPCs, enemies, and bosses**! 🎮
