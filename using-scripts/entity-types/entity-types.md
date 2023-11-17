# Entities

If a game has units, items, or projectiles, it has entities! The term "entity" is a non-specific term used to describe all these game objects.

An entity is just a thing in the game. Your player unit called Human is an entity. A health potion you add to a tower defense game is an entity. Even the individual arrows shot from a bow are entities. (The bow is too!)

It is important to make this distinction. Some places in the editor will refer to specific entities, like units, while other places will use the more broad term "entity" instead.

----

Let's look for example at a **Global Script**. Don't worry if you're unsure exactly what a Global Script is, the important feature to understand is that it can interact with any part of the game, not just one specific thing.

![Global script moving all entities in the game to one position, every second.](img/scripting/globalscriptentities.png)

In this image, you see a script referring to entities. Instead of restricting this script to only work with a certain unit or item, it is written to affect entities. Since this term isn't as specific, that means it can interact with all units, items, or projectiles that are given to the script as "arguments".

"Arguments" is just a coding word that means things that are passed to the script that you want the script to impact.

## Entity Types

When we talk about entity types, we are referring to the different game objects that you can create in a game. In the game engine, this includes units, items, and projectiles. So the entity type of a unit is: Unit.

You can see more about each entity type here:

* [Unit](using-scripts/entity-types/unit.md)
* [Item](using-scripts/entity-types/item.md)
* [Projectile](using-scripts/entity-types/projectile.md)

## Entity Scripts

Another term you may hear is "Entity Scripts". You can view information about the **Script Editor** on its own page. The important thing to note is the use of the word entity. Entity scripts are the scripts that are specific to individual entities. Each entity type can have their own entity scripts. The term entity is used to note that these are not general--or global--scripts.
