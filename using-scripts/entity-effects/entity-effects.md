# Entity Effects

Each entity in the game comes with a collection of **Entity Effects** settings. To access these settings, select an entity, and in the **Edit** window, navigate to the **Effects** tab. These can be confusing at first glance, so we'll at what these options all mean. 

On the left side of the window, you can see options that are all prefixed with 'On'. These work similar to triggers in the script editor. When this event happens to the selected entity, the provided effects will be run. Different entity types have different effect triggers, so it is important to note that the **Effects** tab of a unit type will not look the same as that of an item type. Now let's take a look at all of these events and learn when they occur.

```OnAttacked``` This option only exists for unit types. It runs when a unit is attacked in any way by another unit.

```OnCreate``` This option exists for all entity types. It runs when the entity is created.

```OnDestroy``` This option exists for all entity types. It runs when the entity is destroyed.

```OnIdle``` This option only exists for unit types. It runs when a unit stops receiving movement commands.

```OnMove``` This option only exists for unit types. It runs when a unit receives a movement command.

```OnUse``` This option only exists for item types. It runs when an item is used.

All of these entity effects share four settings. We will look at what each of these does. A fifth setting, ```Tween``` is only used by a few of these events. It will be explained at the end.

When an event occurs, we can tell the game to create a projectile at the position of this entity. ```Projectiletype``` gives us a choice of which projectile will be created when the effect event occurs.

```Sound``` provides the ability to play a sound from the existing sounds in our game in response to the event.

If we want to tell this entity to play an animation when our event happens, the ```Animation``` setting lets us choose from the existing animations in the game.

These events can also be used to trigger specific scripts, either global or entity-based. ```Runscript``` shows a drop-down list of the scripts available to this entity as well as global scripts.

```Tween``` is an option for ```OnAttacked```, ```OnIdle```, ```OnMove```, and ```OnUse```. 'Tweening' or 'in-betweening' is a term used for movements that happen in between frames. This is a simple way to provide common visual effects without having to create special animations.  Here, you can choose from preset options like weapon swings, wobbling, and recoil. For the ```SwingCW``` and ```SwingCCW``` choices, the extra letters are for 'Clockwise' and 'Counterclockwise'. These define the direction the 'Swing' tween moves.

As an important final note, it should be restated that these effects will only apply to entities of the entity type on which they are set. 'Entity Effects' are specific to the entity type, so they will only be run when the 'On-' event involves an entity of that type.




