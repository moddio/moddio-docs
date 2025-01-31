# Items

Items in the game serve as **interactive objects** that units can hold, use, or equip. They play a crucial role in defining **weapons, consumables, armor, and tools** that enhance gameplay mechanics.

## Item vs. Item Type

There is a distinction between **Item** and **Item Type** that applies to all entities:

- **Item**: An **individual instance** of an object that exists in the game world (e.g., a health potion held by a player).
- **Item Type**: The **template or definition** that specifies the properties of all instances of that item (e.g., the health potion's effects, stack limits, and description).

By defining an **Item Type**, you create a reusable blueprint that dictates how each spawned instance behaves.

---

## Creating an Item

To create an item:

1. Navigate to **Entities → Items**.
2. Click on **"Add Entity"** to define a new **Item Type**.
3. Choose an **Asset Selection** (determines item behavior).
4. Configure attributes, states, animations, and body types.

![Items Panel](Imgs/item1.PNG)

---

## Asset Selection

When creating a new **Item Type**, you can choose from different **default behaviors**:

![Asset Selection](Imgs/item2.PNG)

| Option               | Description |
|----------------------|-------------|
| **Unusable Item**  | An Unusable Item that is used as the base for all items. |
| **Rotating Weapon**  | A weapon that rotates to face the mouse cursor. |
| **Ranged Weapon**    | A rotating weapon that fires projectiles (like a bow). |
| **Melee Weapon**     | A close-range weapon with a hitbox for attacks. |
| **Consumable**       | An item that is used and disappears (e.g., health potion). |

---

## General Settings

Each item has **core settings** that define its **appearance, behavior, and inventory interaction**.

![General Item Settings](Imgs/item3.PNG)

| Property            | Description |
|--------------------|-------------|
| **Name**           | The name of the item type for reference. |
| **Sprite**         | The visual representation of the item. |
| **Inventory Icon** | Overrides the default sprite when displayed in the UI. |
| **Description**    | A short text explaining what the item does. |
| **Default Quantity** | The starting amount when spawned (e.g., ammo count). |
| **Max Quantity**    | The limit for how many can be stacked together. |

---

## Inventory & Usage Controls

### Pickup & Usage Rules

![Inventory Controls](Imgs/item4.PNG)

| Setting                     | Description |
|-----------------------------|-------------|
| **Permitted Inventory Slots** | Limits which slots the item can be placed in. |
| **Unit Cannot Drop This Item** | Prevents the item from being discarded. |
| **Can Merge** | Allows stacking with similar items. |
| **Backpack Allowed** | Determines if the item can go into a **backpack**. |

### UI & Input Behavior

| Setting                        | Description |
|--------------------------------|-------------|
| **Flip Sprite Horizontally**   | Flips texture based on direction. |
| **Rotate to Face Cursor**      | Rotates the item to align with mouse aim. |

---

## Bonus & Passive Effects

![Bonus & Passive Effects](Imgs/item5.PNG)

| Setting        | Description |
|---------------|-------------|
| **Passive Effects** | Items that grant passive bonuses when equipped. |
| **Player Attributes** | Changes specific stats for the player. |
| **Unit Attributes** | Adjusts stats for a unit (e.g., +10% movement speed). |
| **Disabled in Backpack** | Determines whether the effect is active inside the inventory. |

---

## Effects & Triggers

Items can **activate effects** when used.

![Effects and Triggers](Imgs/item6.PNG)

| Effect Type        | Example |
|------------------|---------|
| **On Use**       | Healing effect when consuming a potion. |
| **On Hit**       | Apply **fire damage** on weapon strikes. |
| **On Equip**     | Grants a speed boost when holding a specific item. |

Effects can be **linked to states**, ensuring they **only trigger** under the right conditions.

---

## Consumable Items

When selecting the **Consumable** item type, a new tab opens to configure its settings.

![Consumable Settings](Imgs/itemconsumable.PNG)

| Setting             | Description |
|---------------------|-------------|
| **Delay Before Use** | Time before the item can be used after selection. |
| **Cooldown (Fire Rate)** | The delay before the item can be used again. |

---

## Weapon Items

When selecting **Weapon** (Melee or Ranged), a specialized tab appears for configuring its behavior.

![Weapon Settings](Imgs/itemweapon.PNG)

### Weapon-Specific Settings

| Property         | Description |
|-----------------|-------------|
| **Type** | Choose between **Melee** or **Ranged** weapon. |
| **Damage Hitbox** | Defines the **area where melee attacks apply damage**. |
| **Cooldown (Fire Rate)** | Controls how fast the weapon can attack. |
| **Bullet Type (for Ranged)** | Defines the **projectile type** the weapon shoots. |
| **Recoil Force (for Ranged)** | Determines **knockback effect** when shooting. |
| **Deploy Method** | Specifies how bullets appear when fired. |

---

## Key Takeaways

- **Items are essential for gameplay**, defining weapons, consumables, and tools.
- **Attributes and Variables** allow dynamic item behaviors.
- **States and Animations** ensure items visually change based on use.
- **Weapons have unique physics and projectile settings**.
- **Effects can be triggered** when used, equipped, or interacted with.

With these detailed configurations, you can create **complex and dynamic items** for your game! 🚀

---
## Extra Settings

![Extra Item Settings](Imgs/item7.PNG)

| Setting                      | Description |
|------------------------------|-------------|
| **Projectile Stream Mode**   | Controls how projectiles are **synced online**. |
| **Lifespan When Dropped**    | Determines how long an item stays on the ground. |
| **Remove When Empty**        | Whether an item disappears when depleted. |
| **Is Used on Pickup**        | Triggers instant use upon collection. |

Example: A **health pack** might **heal instantly** when a player walks over it.

---
