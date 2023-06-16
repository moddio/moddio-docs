# Bodies

Within the game, there are settings for each Entity type that govern size, shape, and some of its behaviours. On the **General** settings tab for any entity, you will find an option ```Body types```. Selecting an existing body or creating a new one will lead you to the window seen below. You will see a slightly different **Edit bodies** window, depending on which Entity type you are editing: **[Unit](../entity-types/unit.md)**, **[Item](../entity-types/item.md)**, or **[Projectile](../entity-types/projectile.md)**. The first choices offered will be mostly consistent, and we will look at those first.

![Edit bodies window](img/bodies/edit_bodies_top_half.png)

This image shows the body creation options of a Unit. First you have the option to rename the body. Setting ```Name``` to something descriptive is important. You never want to find yourself in a situation where you are looking through available bodies and have no idea what one is supposed to be doing. Let's begin an example here where we will create a body that will be used when we want our Unit type to become very large. In the name area, we enter 'Big Unit'.

Our next option decides how this Unit type will behave in the physics simulation. ```Type``` informs the engine how other entities are able to interact with this entity. Here, we can set whether we want this body to be ```static``` or ```dynamic```. A dynamic body will respond to any forces it is given. This includes both internal and external forces. 'Internal' forces are going to be the actions that are used to move this entity. For units, think about the movement method. Items have an internal force when they are dropped and pushed in front of the dropping unit. With projectiles, something similar to movement method exists. How the projectile is deployed would be considered an internal force.

External forces are easier to understand. Any forces from interactions with other entities are considered. When another unit pushes up against this unit, a ```dynamic``` body will receive that force and respond according to the physics settings. The same applies to items and projectiles. With this ```Type``` of body, our entity reacts to what is applied to it.

On the other hand, there are ```Static``` entities. These will not *move* in response to the above forces, either internal or external. The only way to move these is through script actions. However, these bodies still exist in the physics simulation. We will talk about 'friction' and 'restitution' later. For now, know that if an entity collides with a static unit, it will be stopped or bounce away. If you have rocks or trees in your game, a static body works well. You want nothing to be able to move through it, but you still want to know if something collides with it. The 'Hunt and Gather' template displays this behaviour by default. If the unit swings its axe at a rock, it will collect stone, but the unit is not able to move into or past the rock.

Though not available for units, items and projectiles have another option, ```sprite-only```. With this setting, we can make an entity invisible to the physics simulation. It will not respond to any forces at all, and it is essentially just an image. A great example of this can be seen in many of the default items in the template games. The ```selected``` body type has a Type value of ```sprite-only```. When the item is selected, it doesn't interact with any of the forces within the game, instead it moves wherever the unit carrying it goes. If any entity collides with the item, nothing happens. The entity will go through the item since it is just a sprite and not a physics body.

It is important to note that the ```sprite-only type```, when selected, will disable a lot of the settings in the **Edit bodies** window, removing them from view. If you click on a default ```selected``` body type for an item, you will see fewer options in this window. Select a ```Type``` of ```dynamic```, and all of the physics-related settings will reappear.

The ```Width``` and ```Height``` of a body determines the size of the physics collider as well as the size of the sprite. There are ways to change the size of the sprite so that it is different from the collider, but by default, the sprite for the entity will be the size set here in the **Edit bodies** window.

On the right, you can see the ```original``` dimensions of the sprite that is uploaded to the Entity type. If you are using a cell sheet with multiple frames, the size of the entire image will be displayed here. If you divide it by the number of columns and rows, you have the original size of an individual frame for the sprite.

Let's look at the ```default body``` for the 'Homie' unit type in the 'Open World' template. Here we see that the original size of the sprite is ```128``` by ```128```, but the body dimensions have been set to ```50``` by ```50```. Both the physics collider and the unit sprite will be this size.

Below body dimensions, you will find ```Z-index```. When making your game, the map has different **Layers**. These are named **floor1**, **floor2**, **walls**, **debris**, and **trees**. **floor1** is the lowest and **trees**, the highest. Here, 'lowest' means that anything 'higher' will be displayed above it. This concept is the same with the ```Depth``` setting. Entities with a depth of ```4``` are rendered on top of entities with a depth of ```3```. However, this only applies to entities within the same layer. An entity on layer floor2 with a depth of ```9``` will be covered up by an entity on the trees layer with depth ```1```.

**Notes:** Items have Jointtype, Unit Anchor, Item Anchor






