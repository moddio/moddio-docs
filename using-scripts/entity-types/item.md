# Item

*This page needs help. Find out how to contribute [here](../../how-to-contribute.md)*

Unit interactions are not limited to abilities. Items can be used to further a units capabilities and give more specific actions to the game and its players. These can be weapons, trinkets, armors, and consumables. Anything that a unit can possess or hold is best outlined with an **Item Type**.

There is an important distinction between **Item** and **Item Type**, and it holds true for every entity. In the game, items are the individual instances. The health potion held by my unit is a different item than the health potion held by yours; however, since they are both health potions, they are most likely the same item type. In this scenario, the **Item Type** for health potion is where we set the details for every health potion in the game.

To start, lets look at the **Open World** template. By default, there are no item types in this game, so lets create a new one.

![List of entity types for Open World template](img/Item/entities_open_world.png)

In the **Entities** window and on the header for **Items**, click on the ```Add Entity``` button to begin the creation of a new Item Type.

## Asset Selection

This is the first step for creating an item type. You could select any of the four options here, but these are provided to help you start. The choices will provide different default settings to aid in faster item creation.

![Different choices for default item settings](img/Item/default_item_choices.png)

We will break these down briefly so you can get an idea of what they mean. ```Rotating Weapon``` and ```Ranged Weapon``` define an item that will rotate to face the mouse cursor along with the unit. Rotating weapon sprites will flip horizontally based on whether the mouse is on the left or right side of the screen. These are both set to the ```sprite-only``` body type by default, but the ranged weapon is connected to the unit with a ```Weld Joint```. If the item is set to have a body in the physics simulation when it is selected, the rotating weapon and  unit will behave as the same body. The ranged weapon does not have this joint, allowing it to act independently of its unit within the physics simulation.

A ```Melee Weapon``` has default properties that are useful for melee interactions. They have no ammunition or quantity, instead having a hitbox that determines the area the item will act on when used.

```Consumable``` items do not have projectiles or hitboxes. Instead, these items are set to stack in the unit's inventory, and are consumed on use. If we were making the health potion item type from the example above, this would be the best place to start.

## General

### Name & Sprite

The first options on the **General** tab of the item type settings are ```Name``` and link to ```Change CellSheet```. Changing the name of the item type allows you to better organize your game and keep track of what the item type does. Let's make a simple bow and arrow! In the name field, we will provide 'Bow', then select the ```Change CellSheet``` option.

![Page two of the Assets Library for items](img/Item/Assets_Library_pg_2.png)

A window with the title **Select Image** should appear, and you will see the **Assets Library** first. Here we can choose from many provided images to use for our 'Bow'. For this example, we will select page two of the Assets Library and select 'Scribble Bow' as the image for this item type. 

![The 'Upload from Computer' interface](img/Item/Upload_from_computer_screen.png)

Additionally, you can upload your own asset to use as the sprite for this item type by clicking on the Upload from computer tab near the top of the window. If you wish to upload your own image, you will have to confirm that you are not violating copyright rules and have permission to use the image. There is also an option to allow other creators to use the asset by making it public.

```Column Count``` and ```Row Count``` are more advanced options that allow for animation of the sprite. We don't have to upload an image with just one frame. This process will be discussed more in the **ANIMATION LINK** section. Leaving these counts at their default values of ```1``` means that it is a single, one-frame image and we do not intend to have animations.

![Example 'Bow' item type](img/Item/Bow_item_type.png)

Above, you can see what the window looks like after we have changed the name and sprite for this item type. Note that the item details have been saved, so the name at the top of the window has changed. This will continue to be the example in the following sections.

### Attributes

By default, new item types will have no **Attributes**. These are special variables that have built-in tracking and regeneration, making them more specialized than the entity **Variables** covered in the next section. To add a new attribute, click in the text field and select ```Add new attributes```. You should see the **Edit attributes** window. Here, we will create an example, 'Durability' attribute.

![Creating a new Attribute](img/Item/create_new_attribute.png)

For a more in-depth explanation of Attributes, check out the dedicated documentation **here [attributes link]**. 

The first setting we will change is the attribute's ```Name```. In the text field, simply enter the new name. As with the item type's name, this can be useful for keeping track of what the attribute will do. Everywhere else in the editor, we will now access this attribute by its name, 'Durability'.

Next, the ```Default value``` and ```Value range``` settings allow us to set the starting value of the attribute and clamp the range of allowed values, respectively. Our brand new 'Bow' will start out in perfect working condition, and to better understand this concept, we will leave the default value and maximum value as ```100``` and the minimum as ```0```. Think of this as a percentage. If we changed the max value to ```200```, then a 'Bow' with an attribute value of ```100``` would have ```50%``` 'Durability'.

```Datatype``` gives us the ability to choose whether this attribute should be considered a ```Number``` or a ```Time``` value. Given the built-in processing included with attributes, unlike variables, they are more limited in data type.

**I think we should remove TIME attributes**

### Variables

### Inventory Icon

### Type

### States

### Animations

### Body Types

### Quantity

### Description

### Can be Carried/Used By

## Controls

### Permitted Inventory Slots

### Unit Cannot Drop this Item

### Can Merge

### Backpack Allowed

### Flip Sprite Horizontally with Mouse

### Rotate to Face Mouse Cursor

## Weapon (Ranged)

### Bullet Type

### Projectile Type

### Bullet Speed

### Deploy Method

### Recoil Force

### Bullet Start Position

## Weapon (Melee)

### Damage Hitbox

## Weapon (Ranged & Melee)

### Cooldown (Firerate)

### Delay before Use

## Weapon (Costs)

### Quantity

### Unit Attributes

### Player Attributes

## Weapon (Damage)

### Unit Attributes

### Player Attributes

### Targets Affected

## Bonus

### Unit Attributes

### Player Attributes

### Disabled in Backpack

## Effects

### Triggers

**link to universal effects page**

## Extra

### Projectile Stream Mode

### Lifespan when Dropped

### Remove when Empty

### Is Used on Pickup

### Ignore Server-Streamed Fire Event

### Confined within Map Boundaries








