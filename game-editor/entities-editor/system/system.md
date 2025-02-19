## What’s in the System Folder?

The **System** folder (sometimes shown as **System** or **World** in the editor) is divided into several key sub‐folders that define global behaviors, how players function, and more. Here’s a quick rundown of each:

## 1. Environment

This is the broadest, most foundational category. Inside **Environment**, you’ll often see subcategories like:

- **Global Variables** — accessible anywhere in your game, for storing shared data such as scores, timers, or game states.
- **Regions** — defined areas on your map (rectangles or polygons) used for triggers (e.g., `entityEntersRegion`) or special zones (safe zones, spawn zones, quest areas).
- **Attributes** — customizable named data types (e.g., “Health,” “Mana,” “Strength”) that you can apply to Entities.
- **Entity Vars** — default or custom variables on individual Units, Items, or Projectiles.
- **Bodies** — define collision shapes or physics bodies (e.g., circular or rectangular).
- **States** — reusable conditions like “Stunned,” “Poisoned,” or “On Fire.”
- **Animations** — collections of frames (e.g., “Idle,” “Run,” “Attack”) attachable to Entities.
- **Unit Type Groups** / **Item Type Groups** — grouping multiple Units or Items for shared logic.
- **Secret Variables** — hidden or special-purpose variables (like puzzle solutions).

**Relationship to Other Folders**  
The **Environment** is the root for global data. Anything defined here (like an Attribute or Region) can be referenced throughout the game—whether by Items, Projectiles, or Units.



[**Go to the Environment page →**](game-editor/entities-editor/system/Environment.md)

## 2. Player Types

Defines how players (human or AI) function in your game. For instance, you might have multiple classes or factions:

- “RedTeamPlayer”
- “BlueTeamPlayer”
- “Warrior,” “Mage,” etc.

Each Player Type can have specific **Attributes**, **Bodies**, or custom **Animations**.

**Relationship to Environment**  
- A Player Type might reference Attributes (e.g., “Health,” “Mana”) or Animations from **Environment**.  
- Player variables can also connect to Global Variables (e.g., track total kills in a global scoreboard).

[**Go to the Player Types page →**](game-editor/entities-editor/system/PlayerTypes.md)

## 3. Dialogues

Used for NPC conversations, quest text, or multi-step text interactions:

- Supports branching paths, conditions, and results (like awarding items or updating a quest variable).

**Relationship to Environment & Units**  
- Often triggered when interacting with a Unit (NPC).  
- Can set or read Global Variables (e.g., `questProgress`) or alter an NPC’s State.

[**Go to the Dialogues page →**](game-editor/entities-editor/system/dialogue.md)

## 4. Shops

Manages in-game shops, vendors, or trading logic:

- Define which Items are sold, their prices, and any special conditions.
- Typically assigned to a “shopkeeper” Unit or opened via the UI.

**Relationship to Items & Units**  
- A Shop sells Items (from the **Items** folder).  
- A “shopkeeper” Unit or Dialogue can open the Shop UI.

[**Go to the Shops page →**](game-editor/entities-editor/system/Shop.md)

---

### Putting It All Together
- **Environment**: your global data & definitions  
- **Player Types**: specialized units or AI controlling the game’s “players”  
- **Dialogues**: conversations/quest text systems  
- **Shops**: buy/sell system for in‐game items  

By splitting each into its own sub‐folder, you can quickly manage the entire game’s logic: from universal collisions and stats in **Environment** to how players spawn (in **Player Types**), or how your NPCs talk (in **Dialogues**), and how items are sold (in **Shops**).
