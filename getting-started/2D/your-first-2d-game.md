# Your First 2D Game: Wilderness Survival

In this tutorial, you'll create a complete hunting and gathering game using Moddio's template system. By the end, you'll have a game with:

- Player movement and combat
- AI predators (Bear) and prey (Wild Boar)
- Resource gathering and loot drops
- Health system and blood effects
- Functional weapons shop
- Basic survival mechanics

![Game Preview](img/template1.PNG)

## Prerequisites
- Basic understanding of Moddio Editor
- The "Wilderness Survival" template installed
- Familiarity with visual scripting concepts

## Contents
1. [Project Setup](#project-setup)
2. [Player Character Configuration](#player-character)
3. [Combat System](#combat-system)
4. [AI Behavior Configuration](#ai-configuration)
5. [Loot System](#loot-system)
6. [Shop Implementation](#shop-integration)


---

## 1. Project Setup <a name="project-setup"></a>

Start with the pre-built template:
1. Create New Project → Templates → "Blank Template"
2. Explore initial components:
   - `Homie` In `Units` folder (character controls)
   - `Items` folder
   - `Projectiles` folder
   

<div style="text-align: center; margin: 20px 0;">
  <img src="img/template2.PNG" alt="Project structure" style="width: 300px;">
  <br><em>Blank Template Game</em>
</div>

---

## 2. Player Configuration <a name="player-character"></a>

### Movement Setup
1. Open *Homie Controller*
2. Navigate to *Controls Settings*
3. Explore Settings

<div style="text-align: center; margin: 20px 0;">
  <img src="img/movement1.PNG" alt="Movement settings" style="width: 800px;">
  <br><em>Movement configuration panel</em>
</div>


---

## 3. Combat System <a name="combat-system"></a>

1. **Weapon Configuration**
   - Create *Items/Weapons* folder
   - Create *Melee Weapon Item*
   - Select weapon to modify
   - Adjust damage values in properties panel

<div style="text-align: center; margin: 20px 0;">
  <img src="img/combat1.PNG" alt="Weapon settings" style="width: 600px;">
  <br><em>weapon configuration</em>
</div>

<div style="text-align: center; margin: 20px 0;">
  <img src="img/combat2.PNG" alt="Weapon settings" style="width: 800px;">
  <br><em>weapon configuration</em>
</div>
<div style="text-align: center; margin: 20px 0;">
  <img src="img/combat3.PNG" alt="Weapon settings" style="width: 800px;">
  <br><em>weapon configuration</em>
</div>

---

## 4. AI Configuration <a name="ai-configuration"></a>

### Bear (Predator)
1. Open *AI/Animals/Bear*
2. Set behavior parameters:
   - Enable AI: *True*
   - Sensor Radius: *150px*
   - Idle Behavior: *Wander*

<div style="text-align: center; margin: 20px 0;">
  <img src="img/AI1.PNG" alt="AI" style="width: 600px;">
  <br><em>AI configuration</em>
</div>
<div style="text-align: center; margin: 20px 0;">
  <img src="img/AI2.PNG" alt="AI" style="width: 1100px;">
  <br><em>AI configuration</em>
</div>

### Pig (Prey)
1. Open *AI/Animals/Pig*
2. Configure flee behavior:
   - Enable AI: *True*
   - Sensor Radius: *150px*
   - Idle Behavior: *Wander*

<div style="text-align: center; margin: 20px 0;">
  <img src="img/AI3.PNG" alt="AI" style="width: 1100px;">
  <br><em>AI configuration</em>
</div>

### Spawn Units
1. Open *World Script*
2. Configure Script:

<div style="text-align: center; margin: 20px 0;">
  <img src="img/AI4.PNG" alt="AI" style="width: 1100px;">
  <br><em>AI configuration</em>
</div>
---

## 5. Loot System <a name="loot-system"></a>

1. Open *Items* folder
2. create an item you want
3. write a script so units drop this item

<div style="text-align: center; margin: 20px 0;">
  <img src="img/UnitDeath.PNG" alt="Loot configuration" style="width: 1200px;">
  <br><em>Loot table interface</em>
</div>

---

## 6. Shop Setup <a name="shop-integration"></a>

1. Create New Shop:
   - Right-click *Shops* folder
   - Select "Add New"

2. Add Shop Items:
   - Click *Add Item* in the "Item Types" section
   - Set prices in the item

<div style="text-align: center; margin: 20px 0;">
  <img src="img/shop1.PNG" alt="Shop configuration" style="width: 750px;">
  <br><em>Shop inventory management</em>
</div>


---

# Next Steps
- [Video Tutorial: Full Setup Walkthrough](https://www.youtube.com/playlist?list=PLNN5LDYTMuZgfDOXHXaFB7jXmB-N8UrXZ)
- Experiment with different animal behaviors
- Create weapon upgrade paths
- Create an NPC to open the shop