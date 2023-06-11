# States

*This page needs help. Find out how to contribute [here](../../how-to-contribute.md)*

When controlling how the entities in a game interact and behave, there are specific adjustments you can make to customize things like animations, bodies, and sound. **States** can do all of this, but in a more powerful and easier to manage system. You can create a combination of these settings and define them in a state. When you want your entity to have these behaviours, a script action can change the state of the entity.

Naming is very important with states. When creating scripts that alter the state of an entity, the state will be selected based on this **Name** setting. Try to give your states detailed names that offer clues about their functionality. If we made a state called 'Running' for a unit type, when we looked at our collection of states at a later time, this descriptive name should help us understand what the state does.

The **Animation** setting of a state controls what animation will be played when an entity first changes to this state. There are important details about how the system operates. First, if the animation is set to loop a finite number of times, it will stop playing once it has looped that many times. The animation will not change until a script action or entity effect tells it to. On the other hand, if an animation for a state is set to loop infinitely, it will play until the state changes or the animation is changed through a script action or entity effect.

For an in-depth explanation of **Animations**, visit the [Animations](../animations/animations.md) page.

Here you can select what **Body** the entity will use when it has this state. The body details have a number of settings to customize the appearance of the entity and how it behaves in the physics simulation. States are the most common way to control which body an entity will use and when it uses it. Look, for example, at the default states on items. You are provided with ```dropped```, ```selected```, and ```unselected``` states. When an item has the ```dropped``` state, it has a physics body that other entities can interact with and a different size that it is displayed. The ```selected``` state makes the body ```sprite-only```, removing the physics body and connecting all of its movement to the unit that owns it. When the item is not selected by the unit that owns it, the ```unselected``` state is used to turn off the display of the item altogether. The unit still owns the item and carries it, but no one will be able to see the item. By customizing the body on states, you can create complex functionality for an entity that can be easily controlled through script actions.

For an in-depth explanation of **Bodies**, visit the [Bodies](../bodies/bodies.md) page.

**Different ways to change state...**



