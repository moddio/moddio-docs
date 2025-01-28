# High-Level “System” Categories

When you open the **Entities** panel in Modd.io, near the top you’ll notice folders commonly labeled under “System” or “World.” Four major “System” folders are:

- **Environment**
- **Player Types**
- **Dialogues**
- **Shops**

These folders define global behaviors, how players or NPCs function, multi-step conversations, and in-game commerce. Let’s examine each in detail.

---

## 1. Environment

This is the broadest, most foundational category. Inside **Environment**, you’ll often see subcategories like:

### Global Variables
> Variables accessible anywhere in your game, for shared data such as scores, timers, or game states.

### Regions
> Defined areas on your map (rectangles or polygons) used for triggers (e.g., `onEnterRegion`) or special zones (safe zones, spawn zones, quest areas).

### Attributes
> Customizable named data types (e.g., “Health,” “Mana,” “Strength”) that can be applied to entities. Setting up an Attribute creates a “blueprint” for variables you might attach to Units, Items, or Projectiles.

### Entity Vars
> Default or custom variables attached to individual Entities (Units, Items, Projectiles). For instance, if every NPC needs a “faction” variable, define it in **Entity Vars**.

### Bodies
> Define collision shapes or physics bodies applied to your Units, Items, or Projectiles (e.g., circular vs. rectangular collision).

### States
> Reusable conditions like “Stunned,” “Poisoned,” or “On Fire.” States might affect movement speed, health regen, etc.

### Animations
> Collections of frames or sprite animations (e.g., “Idle,” “Run,” “Attack”). Attach these to Entities and switch them based on states or behaviors.

### Unit Type Groups
> Group multiple Unit types (e.g., “Monsters,” “Animals,” “Guards”) for applying shared logic or events.

### Item Type Groups
> Similar grouping, but for Items (e.g., “Weapons,” “Potions,” “Treasure”), useful for shared scripting.

### Secret Variables
> Hidden or special-purpose variables not easily viewed by players. Store puzzle solutions or “developer constants” here.

**Relationship to Other Folders**  
The **Environment** is the root for global data. Anything defined here (like an Attribute or Region) can be referenced throughout the game—whether by Items, Projectiles, or Units.

---

## 2. Player Types

Defines how players (human or AI) function in your game. For instance, you might have multiple classes or factions:
- “RedTeamPlayer”
- “BlueTeamPlayer”
- “Warrior,” “Mage,” etc.

Each Player Type can have specific **Attributes**, **Bodies**, and custom **Animations**.

**Relationship to Environment**  
- A Player Type might reference Attributes (e.g., “Health,” “Mana”) or Animations from **Environment**.  
- Player variables can also connect to Global Variables (e.g., track total kills in a global scoreboard).

---

## 3. Dialogues

Used for NPC conversations, quest text, or multi-step text interactions:
- Supports branching paths, conditions, and results (like awarding items or updating a quest variable).

**Relationship to Environment & Units**  
- Often triggered when interacting with a Unit (NPC).  
- Can set or read Global Variables (e.g., `questProgress`) or alter an NPC’s State.

---

## 4. Shops

Manages in-game shops, vendors, or trading logic:
- Define which Items are sold, prices, and special conditions.  
- Typically assigned to a “shopkeeper” Unit or opened via UI.

**Relationship to Items & Units**  
- A Shop sells Items (from the **Items** folder).  
- A “shopkeeper” Unit or a Dialogue can open the Shop UI.

---

# “World” Categories

Below “System,” you’ll typically see three important folders:

- **Items**
- **Projectiles**
- **Units**

These house the actual game objects (often called “Entities”) you place in the world or spawn via events.

## 1. Items

> Tangible objects that players or NPCs can pick up, equip, or consume (e.g., Swords, Potions, Keys).

- Items may have **Attributes** (damage, durability) or trigger **States** (e.g., a “Poison” item).
- Items can use collision **Bodies** defined in Environment.
- Items can be grouped in **Item Type Groups** or update Global Variables when used.

## 2. Projectiles

> Specialized Entities for ranged attacks or thrown objects (Arrows, Bullets, Fireballs).

- Often have flight behaviors, collision rules, impact effects (dealing damage or applying States).
- May use an Animation set (spinning arrow) and a Body type for collision.

## 3. Units

> Typically living or moving Entities: players, NPCs, monsters, etc.

- Can have Attributes (health, speed), States (poisoned), Animations (idle, walk).
- **Player Types** are essentially specialized Units that humans (or AI) can control.

---

## Under the Hood: The “Entity” Concept

In Modd.io, **Items**, **Projectiles**, and **Units** are all types of “Entities” (game objects) sharing:

- Position, rotation, collision settings.
- The ability to use “Entity Vars” or “Attributes.”
- Potential event triggers like `onCollide` or `onSpawn`.

(You may not see a single “Entity” folder—this is just the conceptual parent.)

---

## How They Interconnect

- **Environment** → foundational settings, global data (Attributes, Bodies, States).
- **Player Types** → rely on Environment definitions, define how a player interacts.
- **Dialogues** → reference Environment variables and typically attach to Units (NPCs).
- **Shops** → handle commerce, connected to Items and often triggered by Units or Dialogues.
- **Items** → can be picked up by Units, use Environment collision shapes and can modify global vars.
- **Projectiles** → often spawned by Units or Items; can reference unit Attributes.
- **Units** → everything from player characters to enemies, referencing states, attributes, animations.

---

## Example Workflow

1. **Environment**: Define a global variable `redTeamScore`, a region called `RedBase`, and an attribute “Health.”
2. **Player Types**: Create “RedPlayer” referencing “Health” and a circular collision “Body.”
3. **Units**: Add “Zombie” referencing the same “Health” but with AI logic.
4. **Items**: A “Sword” with `damage` can be purchased in a **Shop** or dropped by a “Zombie.”
5. **Dialogues**: Triggered when a player enters a region near an NPC, referencing global `questProgress`.
6. **Secret Variables**: Possibly store a puzzle solution or hidden boolean to track puzzle completion.

Everything is interconnected through references back to **Environment** (Attributes, Bodies, States), making it easy to share data and logic across your game.

---

## Conclusion

- **Environment**: Your global configuration hub for variables, collisions, states, animations, etc.
- **Player Types**: Specialized definitions for playable or AI-controlled characters.
- **Dialogues**: Manage multi-step conversations or interactions.
- **Shops**: Commercial/trading system tied to Items and NPCs.
- **Items**, **Projectiles**, **Units**: Actual Entities in the world. Each relies on **Environment** resources.
- **Entity**: The conceptual base class that ties them all together.

