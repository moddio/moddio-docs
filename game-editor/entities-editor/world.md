# The World Section

<div style="float: right; margin: 0 0 1em 1em;">
  <img 
    src="Imgs/World.png"
    alt="System Folders Screenshot"
    title="System Folders Screenshot"
    style="width: 600px; height: auto;" />
</div>

Welcome to **The World** section of the Modd.io documentation! Here, you'll learn about the major building blocks that make up your game world. First, let's establish a core concept:

---

## What Are Entities? When to Use Each Type

In Modd.io, **Entities** are the fundamental objects that exist in your game world. They range from visible objects like swords and characters to abstract systems that govern gameplay rules. Here's how to choose which entity type to use:

| Entity Type | Best For | Examples | When to Use |
|-------------|----------|----------|-------------|
| **System** | Global rules & configurations | Environment vars, player classes, shops | When creating game-wide mechanics that affect all players/objects |
| **Items** | Interactive objects | Weapons, keys, power-ups | When players need to collect, equip, or use physical objects |
| **Projectiles** | Ranged/traveling objects | Arrows, fireballs, traps | When creating objects that move through space with collision logic |
| **Units** | Living/moving characters | Players, NPCs, monsters | When creating entities with health, AI, or complex interactions |

### Key Decision Flow
1. **Need global rules?** → Use **System**
2. **Physical object players interact with?** → Use **Item**
3. **Moving object with collision?** → Use **Projectile**
4. **Living character with attributes?** → Use **Unit**

Now let's explore each entity type in detail:

---

## 1. System

**System** (sometimes called "System Folders") is your game's rulebook. Use this for:
- Core environment setup (global variables, physics)  
- Defining player roles (Warrior class, Red Team faction)  
- Creating dialogue trees and shop systems

*Example:* Create a "Day/Night Cycle" in Environment variables that affects all Units.

[**Go to the System page →**](game-editor/entities-editor/system/system.md)

---

## 2. Items

**Items** are your interactive props. Choose Items when:
- Players need inventory management  
- Objects require pickup/drop mechanics  
- You want equippable gear with stat changes

*Example:* Make a "Magic Key" Item that unlocks specific doors when carried.

[**Go to the Items page →**](game-editor/items/items.md)

---

## 3. Projectiles

**Projectiles** handle ranged mechanics. Opt for Projectiles when:
- Objects need trajectory/arc movement  
- You require collision events (hit detection)  
- Creating temporary objects (disappear after impact)

*Example:* Create "Poison Dart" Projectiles that apply a DOT (Damage Over Time) state.

[**Go to the Projectiles page →**](game-editor/projectiles/projectiles.md)

---

## 4. Units

**Units** bring your world to life. Use Units for:
- Playable characters with attributes  
- NPCs with AI behavior trees  
- Enemies with health bars and combat logic

*Example:* Build a "Shopkeeper" Unit that reacts when players approach.

[**Go to the Units page →**](game-editor/units/units.md)

---


## Entities vs Units: Understanding the Difference

In **Moddio**, **Entities** is the broad term for anything that exists in your game world and can potentially interact with other objects. This includes everything from **items** (like coins or swords) to **projectiles** (like arrows or fireballs) to **props** (like barrels or decorative scenery). A **Unit**, on the other hand, is a specific subset of these Entities—generally referring to **living or moving characters** such as **players, NPCs, or monsters**.

Because **Units** are **active** Entities with attributes (like **health**), states (such as **"Poisoned"**), and AI or movement, they have specialized scripts and triggers that wouldn’t apply to static or inanimate objects. For example:

> **"When a unit’s attribute becomes 0 or less"**

This type of trigger **focuses on Units specifically**. If we said 
>**"when an entity’s attribute becomes 0 or less,"** 

we’d also have to filter out non-Unit entities (like **items or projectiles**) to avoid extra, unnecessary checks. By writing **"when a unit’s attribute becomes 0 or less,"** we’re telling the game: **“Only run this script for objects classified as Units,”** which saves time and simplifies the code.

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
