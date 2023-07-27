# Unit

Though these entities can be used for many different things, you will mostly see units as the characters in your game. When you create a new game, if you want the players controlling someone and interacting with the world, the most common way to do this would be through a unit.

Let's look at the template game **Open World**. In this template, whenever a player joins, a unit is created and assigned to be controlled by the joining player.

![Unit creation by script](/img/unit/unit_creation.png)

Here, the unit created is of the unit type 'Homie'. You can see this unit type in the entities tab of the editor.

![Game editor's entity](/img/unit/entities_list.png)

It is important to understand the difference between the unit and the unit type. What we see in this image is actually the unit type. These are used as blueprints for the actual units that will exist in the game. In the "player joined" script, you can see that we are instructing the game to use the "Homie" unit type to create one unit that is an instance of this type. This means that all the details and instructions included in the unit type will be given to the unit created.

Now let's take a look at these "details and instructions" in more depth.

When you click on the `...` next to the unit type on the entities list, you are given a few options. We're going to discuss **Properties**. Selecting this option will open up a new window in the editor. The title of this tab will be "Edit (Unit Type)" . For the above example, the title is "Edit Homie" . You can also access this window by clicking anywhere on the middle or left side of the row in the Entities list

This section will offer descriptions of the different sections of the properties tab. The links provided will offer more specific information related to their use.

## General

On this screen, you can change the name and sprite of the unit type, as well as animations, states and other customizations.

![A Unit's general settings](/img/unit/unit_general_settings.png)

### Name and Sprite

Perhaps the most important setting under the **General** tab is **Name**. In the game editor, you will often need to access different units by their Unit Type. To find the type you are looking for, you use its name. In this example, the name of the type is "Homie".

Right above this option, there is an image preview of the unit type's sprite and a link that says **Change CellSheet**. This is what you click on when you want to change the appearance of units of this type.

In the image above, you can see the default page that is shown when you click on this link. The main tab shown is the **Assets Library**. You can select from any of these unit sprites, and the sprite for this unit type will change to the selected image. We have selected the "Robot Futuristic Human Person" image, and now the **General** tab changes slightly to what you see in the image below.

![Preview of new unit sprite](/img/unit/preview_new_unit.png)

The other tab found when clicking on Change CellSheet is Upload from computer . Most of the time, you will want to use assets in your game that are not in the small asset library provided. This page is where you can do that. The tab can be seen below.

![Upload from computer prompt](/img/unit/computer_prompt.png)

As an easy example, to upload a new image for "Homie", click on the `Upload` button and select the file from your local folders. Let's just use an image -- not a sprite sheet -- so we will leave the `Column Count` and `Row Count` options set to the default, 1.

When the image file is selected, the text area will display its file name to the left of the `Upload`  button. The last thing to do is click `Submit`. Then the **General** tab will appear as it did when we changed the sprite to "Robot", but it will show the image you uploaded instead.

### States

These options are different modes or states that this unit type can have. By default, this area is populated with one state, "default". The state controls the animation and the physics body of these units. In the image below, you can see the default state options.

![State selection](/img/unit/state.png)

In the preview, there are three rows; each of them says "default". The first row is the name of the state. Next to the film strip icon, on the second row, is the animation for the state. The final row, with the human body icon, is the name of the physics body assigned to the state.

By clicking in this window, but not on top of an existing state, you will find a prompt for selecting a state to add or creating a new state. If you have already made the state you want to add, you can select it from the list and it will be added to the state selection area of the properties window for this unit type.

When you select `Add new state`, a window will appear where you can set the details for the state. Options are provided for the state's name, animation and body.

![Right after clicking "Add New State"](/img/unit/add_new_state.png)

As with selecting an existing state, creation of a new state will direct you back to the properties window for the unit type and you will be able to see the new option alongside the rest of this unit type's states.

### Animations

The next option in the unit type customization window is where you select existing animations. You can also create new animations you want to assign to the unit type. Similar to how states were selected, clicking in this area will show a drop-down menu of existing animations, but it will also allow you to create a new animation when you select `Add new animation`. The resulting window can be seen below.

![Empty new animations settings](/img/unit/edit_animations.png)

First you have the option to set the name for the animation. It's a good idea to give your animations and states names that provide a bit of information about its use. For example, if we create an animation for our unit type 'Homie' that plays when the unit is running, we probably want to name the animation 'running' or 'run'.

Next, there is an option to set the 'frames' for the animation. We will go into more detail on these in the advanced 'cellsheet' tutorial. The area next to frames will display a small image of the frames that will play in the animation. These are displayed in order, from left to right. To add new frames, click on the plus sign to the right of the list of frames. For a simple one-frame cellsheet like the one used for the 'Homie' sprite, you should see something similar to the image below.

![Select frames for an animation](/img/unit/animation_frames.png)

Here you can see what your cellsheet looks like. In our case, it's just our image. Hovering over the image, you can see a gray rectangle. This is used to show how the cellsheet is divided up. To select a certain frame, just hover over the frame that you want to add and click on it.

`Framespersecond` allows you to set how fast you want the animation to run. If we had a four-frame animation, setting this value to 1 would result in the game taking four seconds to play out the entire animation.

Lastly, there is an option for `Loop Count`. This option refers to how many times the animation will play. By default, this area is empty, and you should see "infinite". For something like a running animation, this would be fine. As long as units of this type are running, we probably want to loop the animation.

What if you wanted to play the animation twice? Maybe you have an item called "two loaves of bread" and an animation on your unit type that is used to show the unit eating bread. You could run it once, sure, but this is "two loaves of bread". Here we can set the value to 2 so that when the animation plays, it will loop twice, giving us the appearance of eating two loaves of bread.

### Body Types

This area is formatted the same as animations. The field is filled with all the body types you have assigned to this unit type. Of course, by default, there is one body type, "default". Body types are used for setting the size you want the unit to appear and how you want the unit to interact with the physics of the game.

Clicking on the open space inside the list of body types will give you a list of existing body types and an option to `Add new body`. When creating a new body, a window titled **Edit bodies** will appear. You can see what this should look like below.

![The basics of bodies](/img/unit/edit_body.png)

### Attributes

The classic example for an attribute on a unit is health. In fact, unit types will have two attributes by default, "Health" and "Speed".

These are essentially just extra numbers that are stored on the units belonging to this unit type. Attributes and variables are similar, but there are important differences. When you set an attribute, you have additional built-in features at your disposal. The important differences are the regeneration system and the attribute bars. We will discuss these individually in a moment.

![The Attribute selection setting](/img/unit/attribute_selection.png)

Above is an image of the attributes from our unit type, "Homie". These default attributes also have default values, or numbers that the attributes are set to when the unit is created (for example right after a game server is restarted). When you create a new unit of type "Homie", the health attribute of the unit is set to 100 by default.

By clicking in the empty space within the attribute list, you have the option to add existing attributes to the unit type, or you can select `Add new attributes` and a window titled **Edit attributes** will appear. You can see what this looks like in the image below.

![A new empty attribute](/img/unit/empty_attribute.png)

Let's go through each of the options provided here. To do so, we will create a new attribute on our unit type "Homie". What if our unit type is having a bad day and is a little bit angry? How about using an attribute to create a "rage meter".

The first option, **Name** is exactly what it sounds like; the attribute needs a name. Here we will enter `Rage`.

Next on the list is **Default value**. In the default attributes, remember this was set to 100 for "Health" and 10 for "Speed". To make it as easy as possible, let's set this to `0`. "Homie" isn't going to be angry at all, at least until something in the game happens.

We need to set some limits on our attribute to make sure its values doesn't get out of control. This is where we will use **Value range**. The two options here, `min` and `max` are used for setting the minimum and maximum values that this attribute can be. For our "Rage" attribute, the default values of 0 and 100 will work perfectly. It's easiest to understand what our "rage meter" represents if we can also think of it as a percentage. When a unit of type "Homie" is created, it is 0% angry; its "Rage" attribute is 0. Since there are now limits on this attribute, it can never be less than 0, the `min`, or greater than 100, the `max`.

`Regeneratespeed` is the next option, and it is the first of the details that make attributes unique from "Variables". The game engine will actually allow for attributes to automatically increase or decrease as time goes on. A good general rule is that a value of 0.25 for this option will increase the attribute by about 1 per second. In the other direction, to decrease the value of an attribute by 1 per second, you would set this option to -0.25.

For the "Rage" attribute, let's set it to `1`. In doing so, the "Rage" of units of type "Homie" will increase by 4 every second. Another way of looking at this would be that the attribute will automatically increase to 100 after the unit of type "Homie" has existed for 25 seconds.

We're about halfway through, so here's what our settings for the new "Rage" attribute should look like so far.

![Halfway through the "Rage" setting](/img/unit/rage_attribute_halfway.png)

Moving on, the next part of what makes attributes unique can be adjusted. The engine has built-in attribute bars that allow players to see attributes and their values directly on the screen. Of course you can have attributes that will not be visible, but for this example we will turn on these options so we can see the "rage meter" working.

**Shown as** is a list of four buttons that allow you to set when and where the attribute bar will be visible. The option `center bar` is different from the other choices. This is specifically an HTML attribute bar that can be displayed in the bottom center of a player's screen. For units of this unit type, only the owner player of the individual unit will see this bar. We will select it. Below you can see how a `center bar` attribute is displayed in-game.

![The in-game center bar display](/img/unit/center_bar_in_game.png)

The other options here are for attribute bars that are shown in-game, beneath the unit they belong to. Player types can have different relationsips like "hostile", "friendly", and "neutral". If we didn't want enemies to see our health bar or our "rage meter", we could leave the option `unit bar(hostile)` unselected and player types that are hostile to this unit's owner's player type would not be able to see it below the unit. Let's just enable them all for this example.

A true or false toggle is our next option beside the label **Display value**. Here, we have the choice to show the actual number value of the attribute within the displayed attribute bar. 

* `False`: Players can see roughly how angry each unit of this type is, but not *exactly* how angry it is. So this would show just a bar below units of this unit type.
* `True`: Players can see *exactly* how much "Rage" the unit has. So this would show the attribute bar and exactly how full it is with an actual number value.

We don't have to show this attribute all the time, though. This is how the next option, `Show When`, is used.

The drop-down list has four options:

* `all the time`: Used if you *always* want to show the attribute bar
* `value changes`: Show the attribute bar briefly whenever the value changes
* `value is greater than min value`: Disable visibility of attribute bar when value is at the minimum
* `value is less than max value`: Disable visibility of attribute bar when value is at the maximum

For this example, we will set `Show When` as `value is less than max value`. Now the attribute bar for "Rage" will be displayed under units of type "Homie" always until the value is at its maximum. In other words, we will see the attribute bar until the 25 seconds have passed and this unit has reached a value of 100 "Rage".

Finally, we have two cosmetic options, **Color** and **Decimal places**. By default, new attributes will be assigned a color value of "white". This is the fill color of both the unit-based attribute bars and the center attribute bar that is displayed for the owner of the individual unit. Just to the right of the field that says "white", you will see a white square. You can click on this square to open up a color picker that will generate a hexidecimal color code for your choice. Rage is commonly associated with the color red, so we could pick a nice custom red color with the provided tool, but for simplicity we will just provide this option with a hex code for a simple bright red, `#ff0000`.

The **Decimal places** setting allows you to display a more precise number inside the attribute bar. By default, no decimal places are shown on the value, but maybe we wanted to increase "Rage" by smaller amounts per second: even smaller than 0 decimal places would be able to show. We could set this option to 2, then the attribute bars for the "Rage" attribute on units of this type would give a more precise reading. The difference would be instead of 25 displayed as the value when this setting is 0, a setting of 2 would show us a value like 24.65 or 24.78. It would give more precise information to the players.

To finish up this example, we will just leave it at `0`. Now that all the settings have been looked at and adjusted, the **Edit attributes** window looks like the image below. Make sure you click the `Save` button to keep all of your changes!

![The completed "Rage" attribute](/img/unit/rage_attribute_complete.png)

When the game starts, we join and are assigned a newly created unit of type "Homie". After a few seconds, we can see that our new attribute is working and our settings have been applied. Another image below provides an example view.

![Our new attribute on display](/img/unit/finished_attribute.png)

### Variables

There will be situations where you want to save specific values for each unit of a certain unit type. We already know that this is possible through attributes, but many cases will only require a simple way to store data. This is where **Variables** shine. They do not have built-in regeneration or display bars, but when we use variables, these add-ons aren't necessary.

Say we are making a deathmatch game, and for each unit of type "Homie", we need to track how many kills a unit has. To start, we click on the variables area, where it says `add variables`. This will display a drop-down list with all existing entity variables in your game. In the "Open World" template, there shouldn't be any to start, so it will just say `Add new variable`.

![Create a new variable](/img/unit/new_variable.png)

The new variable creation window, titled **Add Variable**, provides three customizations. **Key** is essentially the "name" of the variable. In this example, we will call it "Kills".

**DataType** and **Value** are used to define what type of data the variable will store and what the data will be when the unit is created. For "Kills", we want to count a number, so the default, `number`, is what we will use. Since Value is now the number of "Kills" we want all units of this unit type to start at, we set `0` as this default value.

!["Kills" variable example](/img/unit/kills_variable_example.png)

That's it! Now we have a variable on our unit type that we can access within our scripts. There are many different data types that you can set when creating a new variable, so let's look at these briefly.

![Different data types for entity variables](/img/unit/different_variable_types.png)

Since we don't need to display the data as a bar or do regeneration math on it every tick of the engine, we have a lot more freedom. While attributes could only be numbers, these variables can store whatever type of data you want. Some of these options can be left for a more advanced tutorial, but let's look at the simple and more common options.

We know what `number` is, so the next choice is `boolean`. Boolean is a data type that can only be one of two values, `true` or `false`. Another common choice of data type is `string`, which means text. Anything like words, sentences, even empty spaces can be strings. Think of them like strings of characters. Maybe you want to store a nickname for each unit of your selected unit type. You could have a variable called "Nickname" and store it as a string.

That's all for the introduction to variables, but more advanced information can be found here. **[link to adv. variables] edit this**

### Inventory and Backpack Size

The next to options under general settings define the unit type's ability to store items. There are two different locations that items can be stored on a unit, and they are both built in to the game engine.

Units have an inventory and a backpack. Inventory is directly accessible through the number keys corresponding to the inventory slots displayed on the screen. When playing the game, press `2`, and your unit will select the item in inventory slot two. That's only if the `Inventorysize` setting is greater than or equal to 2. By default, this will be 5, but what if we set it to 1? Units of this unit type would only have 1 inventory slot, then pressing 2 would do nothing. See below for an image of the inventory on our "Homie" unit type.

![Unit inventory display](/img/unit/inventory_display.png)

`Backpacksize` sets how many storage slots units of this unit type will have in addition to its inventory. The default setting is 0. This will hide the "Backpack" button in game. Set it to `9` and let's look at what happens.

![The unit backpack display](/img/unit/backpack_display.png)

Now there is a button, `Backpack`. When clicked, you see the image above. Items can be dragged between the inventory and the backpack with your mouse. If a unit's inventory is full, but there is space in the backpack, items will automatically fill out these slots!

### Default Items

So we know units of our chosen unit type will have all of these settings when they are created. The same follows with our last setting, Default Items. We can set each new unit of this type to be created with a certain inventory. By clicking in the area that says Choose defaultItems , we are provided a list of all the items that exist in the game. Any item that we select here will be given to each unit of this type when it is created. The order of these default items matters. Inside the area for this setting, you can drag and drop the items to set the specific order that you want. The first item in the list will go in inventory slot 1; the second will be in slot 2.

The "Open World" template game doesn't start with any items, so we'll visit a different template for an example of this setting.

![Default item configuration](/img/unit/default_item_config.png)

In the "Battle Royale" template, you can see that there are two items included in the "Fighter" unit type's Default Items . The first, "Uzi" is created in this unit's first inventory slot. The "Baseball Bat" can be found in the second.

## Controls and Abilities

Although the name of the section is "Abilities & Controls", this section of the properties tab in the editor is called "Controls." In case you are looking for "Abilities", we have added it here because this is where you will find it. This is the home of *how* the unit type interacts with the world. You can set how the unit moves and add custom keybinds, or abilities, that can be linked to scripts.

### Keybindings (Abilities)

In this area, you can find all of the existing keybindings in the game. Note that these are also referred to as "abilities" in some areas of the editor. By looking at the "Open World" template game, we can see a few default keys connected to pre-made scripts for using, picking up, and dropping items.

![Default keybindings for the template game](/img/unit/default_keybindings.png)

Each blue rectangle corresponds to a specific key or mouse action. The first part of each item is what user action the ability will be linked to. In the example, the first keybind is connected to the `B` key. Next, you will see that you can set scripts for both the `KeyDown` and `KeyUp` events for the connected key or mouse button.

* `KeyDown` triggers when the key is pressed down
* `KeyUp` triggers when the key is released again

In the second item, when Mouse left click  is held down, the `start using item` script runs. When `Mouse left click` is released, the `stop using item` script runs. If there is no script tied to a key action, the setting will display `undefined`.

To add a new Keybinding to a unit type, click in the empty space within the list of existing items. You should see a drop-down list with all of the abilities that have already been made but have not been given to this unit type. At the bottom of the list, click on `Add new KeyBinding` to create a new ability. In the "Open World" template and on the default "Homie" unit type, this will be the only option. The **Edit keybindings** window should appear. This window is shown in the image below.

![Creating a new keybind](/img/unit/new_keybind.png)

The first setting here is the `key` or mouse button that will be connected to this ability. Click on the box to see a drop-down list where you can select from the list of keys available to be connected to abilities. Everything below this option, under **Abilities cast** will only happen when this key is pressed.

As we discussed before, `On key down` runs whenever the key is pressed, and `On key up` only runs once this key is released. Their settings will work the same way, so we will only discuss them once.

**Run script** provides a drop-down list of the scripts available for this unit type. These will be your global scripts and the entity scripts specific to the unit type.

The **Cost** settings determine what units of this unit type have to pay to use this ability. You can set up an ability to cost an amount of an attribute. There are two types of attributes here. **Unit Attributes** belong to the unit that is using the ability. Here, we could set up the new ability to cost 20 "Health".

Let's think about the "Rage" attribute we made in the unit attribute section above. Maybe we have some entity script on our unit type that we call "Calm down". We want this script to only be run when we have a full "Rage" attribute, and we also want it to reset our "Rage" to its minimum, 0. For this example, let's assign this ability to be cast when the `J` key is released after being pressed.

![Unit attribute as an ability cost](/img/unit/unit_attribute.png)

Don't worry about what this script actually does. We are mostly using it as a placeholder to show what the setting does. The important details are the **Cost** settings and understanding how they function.

Since this ability costs 100 "Rage", it can only be used when the unit has a full "Rage" attribute. (The maximum value for "Rage" is 100). Costs are built in, so if the unit can afford the cost, the amount will be automatically removed from the desired attribute. In case the unit can not afford the cost, the user action is ignored and the corresponding script will not run.

We also have the option of connecting **Player Attributes** to be used as ability costs. They work the exact same way, so we won't cover them here.

### Movement method

The physics simulation of the game engine allows for a few different options that control how it calculates movement of a unit. `Velocity` is the default setting for the "Homie" unit type in the "Open World" template. This is the simplest movement method, where the physics engine assigns a speed that the unit is moving in a certain direction. A new velocity overwrites the previous velocity of a unit, so a unit using this movement method can turn immediately.

Another way movement can be simulated is through the application of `Force`. Here, instead of the physics engine assigning a velocity for the unit, the engine will move the unit as if a force was pushing it in the movement direction. This option is better for games where you will have other forces acting on the unit like gravity in platformer games or explosions from rockets. When applying a force in the opposite direction that a unit was moving previously, the force will first cancel out the previous velocity of the unit before it can move into the direction applied.

There will also be times where you have a unit type that you don't want to move at all. Maybe you only want its movement to be controlled by scripts. `This unit will not move` is provided as an option.

### Movement control scheme

Not every game will require its players to play with the same keys. This setting allows for the creator to choose how players will move units of this unit type. Movement in four directions can be controlled with the option `WASD or arrow keys`. You will find this as the default setting in the "Open World" template.

A similar setting offers key controls in only two directions. `AD or Left & Right keys` limits the unit's movement controls to two directions.

You don't just have to rely on a keyboard for movement controls. A third setting, `Constantly move unit toward the mouse cursor`, does exactly what it says. Based on the built-in speed attribute, units of this unit type will always move in the direction of the controlling player's mouse cursor.

For certain cases, it may be useful to disable movement controls altogether. There is an option called `None` for these unit types.

### Absolute Rotation

Units of this unit type can be set to rotate through a full 360 degree range by enabling this setting. Based on the perspective of your game (for example if it uses a top-down camera angle) you may want the unit to be able to face any direction. In a different situation, you may have a platformer game that has a unit type you want to be able to rotate. How about a ball? Enabling this setting will allow the unit to rotate freely allowing for the ball to "roll" around in response to forces.

Disabling `Absolute Rotation` will ignore rotational forces. Units of this unit type, will not "roll" like the ball example, they would instead slide in the direction of the force. You will also see this setting commonly disabled in platformer games because the sprite appears as if the camera is in front of it and not above. In this perspective, we don't want the sprite to rotate in 360 degrees.

### Flip sprite horizontally wrt mouse

This setting considers the appearance of the unit type's sprite. If we want our units to face to the left and right, we don't have to provide two different images. It's simple for the engine to mirror the sprite or "flip" it.

Here, we are concerned about whether the player controlling the unit's mouse is to the left or right of the unit. If the mouse is to the right of the unit, the sprite will not flip. A mouse cursor on the left side of it will "flip" the image, and it will appear as a mirrored version.

### Rotate to face mouse cursor

Enabling this rotation method will have units of this unit type constantly changing the direction they are facing to point at the mouse cursor of the player controlling the unit. An important detail to note  is the direction the sprite for the unit should face by default. For this effect to appear correctly, you will want the image of the unit that you use as its sprite to be facing up, or north. When configured this way, the unit will "look" in the direction of its owner's mouse.

### Mobile version control layout

The last element of the **Controls** tab for a unit type provides a way to customize the interface of your game on mobile devices.

![Mobile game interface customization](/img/unit/mobile_layout_customization.png)

These settings are divided into two parts. On the left side and under Key bindings you will find all of the abilities that belong to units of this unit type. The right side, Mobile Device Canvas represents the screen of a user playing this game on a mobile device. Each item on the rightside canvas can be clicked and dragged around to change the position it will appear in game. By default, movement controls are found on the left, and rotation is on the right.

Items on the left can be clicked. Doing so will remove the ability from the list and place it on the screen preview. Then it can be moved to wherever you like. The above image is for the "Homie" unit type in the "Open World" template. Below is an image of each keybind added to the game and placed in a different spot.

![Custom mobile interface for this unit](/img/unit/mobile_interface.png)

Its important to add new keybinds to the mobile interface. If not provided, mobile players will not be able to use the abilities that are controlled by these buttons. A good mobile layout is functional and not obstructing, meaning that its easy to control the unit and the buttons don't block too much of the player's view.

## AI

Units are not just for human players. The AI or computers in your game can also control and be assigned units. This section of properties features settings used to customize how AI can control this unit type

### Enable AI

By default, unit AI is disabled on unit types. When set to `false`, most configuration settings will be hidden. If you want units of this unit type to be controlled by a computer and not a human player, set this option to `true`. When changed, there will be many more options under the **AI** tab of the unit type. AI can also be enabled or disabled through scripts.

Attack Response to Hostile Units

If set to `None`, these units will do nothing when attacked by units controlled by players that are hostile to the unit's owner. Whether the interaction is `hostile` is determined by the relationship between the players that own the units. A player can be a human or a computer. For more information about these details, check out the **Diplomacy** section of the documentation for **Player Types**.

The `Flee` option will have units of this unit type try to get away from the unit that is attacking it. You could do the opposite with the `Fight` option. These units will respond to attacks by targeting the hostile unit and trying to use its selected item against them.

### Idle Behaviour

When no events are telling these units to do something, the AI-controlled unit is considered to be "idle". This option allows either has the unit do nothing when idle with `Stay`, or it can be set to `Wander` around the game.

### Let Go Distance

After the AI unit has been alerted to something happening in game, you may not want it trying to chase a unit or fight it as it moves anywhere in the map. Here, we are enabled to set a maximum distance that units of this unit type will stay engaged with their target. It should be greater than the `Sensor radius`. If the attacking unit is faster than this unit, we may not want it to be able to drag the AI anywhere in the game. Think of an AI unit type for a "Bear". Consider this like its sense of smell. Once the unit gets far enough away, it cannot smell its target anymore and loses interest.

### Max Attack Range

If units of this unit type have some sort of ranged weapon or item, a limit can be set on the maximum distance from its target to attack. This unit could use the weapon from whatever distance away from the target it can as long as it hasn't been told to `Let go`. If we set a limit with this option, once the distance between this unit and the target is greater than this number, the AI unit will no longer be able to attack.

### Max Chase/Flee Distance

This setting places a limit on the distance an AI unit will chase its target or flee from an attacking target. Once the unit has travelled this farr as a part of its chase or flee response, it will stop the action and return to idle behaviour.

### Path Finding Method

There are different ways to program AI movement. This setting is still in development, so there is only a `Simple` option.

### Sensor radius

A radius is the distance from the center of a circle to any point on its edge. **Sensor radius** uses this logic. Units with AI have sensors that are invisible shapes drawn around them at all times. The center of the shape is the center point of the unit, and this setting determines how big to draw that shape. These work the same way the physics for entities work. They are essentially bodies that are added to the physics simulation and checked for collisions. When something collides with the sensor it doesn't bounce off it like the bodies of entities. Instead, it enters the sensor radius, and the AI unit is told to respond.

### Sensor Response to Hostile Units

When the physics simulation records a unit entering the sensor radius of a unit of this unit type, the AI unit will respond in a few different ways. Setting this value to `None` would result in the unit doing nothing when a hostile unit enters its sensor. In the same way, we set **Attack Response**, we also have the options for `Flee` and `Fight`reactions.

* `Flee`: Unit will try to escape the attacker
* `Fight`: Unit will use its selected item against the unit that entered its sensor

## Effects

On this screen, you have a number of shortcuts for adding effects that are triggered by events that related to your unit. For example, if you want a script to run when units of this type move or are created, you could use this section.

### Triggers

OnAttacked, OnCreate, OnDestroy, OnIdle, OnMove

## Extra

The last location within the **Properties** settings offers a few final details that can be used to customize the unit type. In the old editor, this is where **entity scripts** could be found.

### Is untargetable

### Confined within map boundaries
