# The World Section

<div style="float: right; margin: 0 0 1em 1em;">
  <img 
    src="Imgs/World.png"
    alt="System Folders Screenshot"
    title="System Folders Screenshot"
    style="width: 600px; height: auto;" />
</div>


Welcome to **The World** section of the Modd.io documentation! Here, you’ll learn about the major building blocks that make up your game world—from high-level “System” configurations down to concrete Items, Projectiles, and Units. Each subsection has its own dedicated page (linked below), where you’ll find more in-depth explanations, screenshots, and scripting examples.

---

## 1. System

**System** (sometimes called “System Folders” in the editor) is where you define:
- **Environment** (global variables, regions, attributes, entity vars, bodies, states, animations, etc.)  
- **Player Types** (human or AI roles/classes/factions—Warrior, Mage, RedTeamPlayer, etc.)  
- **Dialogues** (NPC conversations, branching story text, quest dialogue triggers)  
- **Shops** (in-game commerce: setting up items for sale, shopkeepers, prices, etc.)

[**Go to the System page →**](game-editor/entities-editor/system/system.md)

---

## 2. Items

**Items** are tangible, interactive objects in your game world. They can be placed on the map, picked up, equipped, consumed, or collected by players or NPCs. Examples include:
- **Weapons** (swords, bows, guns)
- **Consumables** (health potions, food, power-ups)
- **Quest Items** (keys, artifacts, collectibles)


[**Go to the Items page →**](game-editor/items/items.md)

---

## 3. Projectiles

**Projectiles** are specialized entities for ranged or thrown attacks—think **arrows, bullets, fireballs**, or any object that travels through the air. They can be spawned by:
- A **Player** action (e.g., shooting a bow)
- An **NPC** skill (enemy mage casting “Fireball”)
- A **Script** (wave-based spawns, traps firing arrows)

### Why It’s Important
- **Ranged Combat:** Projectiles enable distance-based gameplay and a variety of combat styles.  
- **Collision & Effects:** They usually have collision logic (deal damage or apply states on impact) and can be animated (spinning arrow, lightning bolt).  
- **Flexible Scripting:** Combine triggers like `when projectile collides with unit` to handle explosion effects, splash damage, or quest objectives (e.g., “destroy the target dummy with an arrow”).

[**Go to the Projectiles page →**](game-editor/projectiles/projectiles.md)

---

## 4. Units

**Units** are generally “living” or moving entities in your game world, including **players**, **NPCs**, and **monsters**. They can have:
- **Attributes** (health, speed, mana, stamina)
- **States** (poisoned, stunned, on fire)
- **Animations** (idle, walk, attack)
- **AI or Player Control** (enemy pathfinding vs. player keyboard input)


[**Go to the Units page →**](game-editor/units/units.md)

---

## Entities vs Units: Understanding the Difference

In **Moddio**, **Entities** is the broad term for anything that exists in your game world and can potentially interact with other objects. This includes everything from **items** (like coins or swords) to **projectiles** (like arrows or fireballs) to **props** (like barrels or decorative scenery). A **Unit**, on the other hand, is a specific subset of these Entities—generally referring to **living or moving characters** such as **players, NPCs, or monsters**.

Because **Units** are **active** Entities with attributes (like **health**), states (such as **"Poisoned"**), and AI or movement, they have specialized scripts and triggers that wouldn’t apply to static or inanimate objects. For example:

> **"When a unit’s attribute becomes 0 or less"**

This type of trigger **focuses on Units specifically**. If we said **"when an entity’s attribute becomes 0 or less,"** we’d also have to filter out non-Unit entities (like **items or projectiles**) to avoid extra, unnecessary checks. By writing **"when a unit’s attribute becomes 0 or less,"** we’re telling the game:  
> **“Only run this script for objects classified as Units,”**  
which saves time and simplifies the code.

### Summary:
- **All Units are Entities, but not all Entities are Units**.
- **Units** = Characters that **move, attack, or have AI and health**.
- **Entities** = Everything in the game world, including **static items, projectiles, and scenery**.

---

## How These Pieces Fit Together

All four subsections—**System, Items, Projectiles, and Units**—collectively shape your game world. Here’s a quick example of how they interconnect:

1. You define **Attributes** (like “Health”) in **Environment** (under System).  
2. A **Player Type** (Warrior) uses that Health attribute, and can equip an **Item** (Sword).  
3. The sword might spawn a **Projectile** (a slash effect or arrow).  
4. Both the sword and projectile might apply **States** (e.g., “Poisoned”) to a **Unit** (enemy NPC).  
5. A **Dialogue** in System might trigger after defeating that NPC, and you might set up a **Shop** selling more powerful swords.

By splitting each topic into its own page, we hope you can deep-dive into the mechanics that matter most to you without scrolling through a single massive doc. Click through the links above or use the sidebar to learn more!
