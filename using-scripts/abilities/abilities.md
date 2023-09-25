# Abilities

The **new** abilities system is designed to expand on the old abilities system found within `Keybindings`. Previously, you would add or edit a key and within the customization for this 'ability', edit what is triggered by the key event.
Keybindings have worked well enough, but they were fairly limited in what they could accomplish. The old system provided options for built-in `attribute` cost(s) and a `script` that would be triggered by the key event.
Abilities (this will refer to the new system from now on) were built to give both more power and more freedom to the creator. The main differences are as follows:

- Abilities are broken up into the events `startCasting` and `stopCasting`. These are triggered independently.
- Abilities do not **need** to be triggered by a key event. You can package all of your desired functionality into an ability that doesn't even require a key press.
- A single ability packages the scripting logic for the entire lifecycle of the cast. Since start- and stopCasting events belong to the same ability, the ability's behavior is easier to understand.
- The attribute cost system from keybindings (old abilities) is included and behaves the same in Abilities.
- Abilites have built-in features that offer more control from an easier access point. `castDuration` and `cooldown` provide ways to automatically manipulate a unit's interaction with an ability.
- Abilities have an optional icon image that can be used to customize the user interface. These icons become the display for the ability button on mobile devices.

### What you will find in the editor

Abilities in the editor are shown in two different localtions. When editing a unit type, under `Controls`, there is a new field `Abilities` where you can add existing- or create new abilities that belong to a specific unit.
Like other enumerations in the editor, abilities are also reflected globally. A global ability interface can be created and used as a skeleton to quickly apply an ability to multiple unit types.

There are key differences, though. Creating an ability from the unit type editor will also create a global ability to match, but inspecting this global ability will show that all entity scripts have been removed.
Entity scripts are not available as global scripts, so global abilities cannot use them. A global ability *can* use global scripts.

If you want to use an ability on multiple unit types, you will have to either add new entity scripts to the ability in the unit type editor or use global scripts.

### The anatomy of an Ability

- `Name`:  what the ability is called in the different editor windows
- `Event scripts`:  (Optional)
    - `Start casting`: the script ([G] Global or [E]) Entity that runs when 'start' is triggered
    - `Stop casting`:  the script ([G] Global or [E]) Entity that runs when 'stop' is triggered
- `Cast duration`: (Optional) if set, `stopCasting` is triggered automatically, this many milliseconds after `startCasting` was triggered
- `Cooldown`: (Optional) if set, this ability cannot be cast again until this many milliseconds after `startCasting`
- `Cost`: (Optional) the same attribute cost interface as the keybindings system. `startCasting` will fail to trigger if the unit does not have this amount of these attributes
- `Stream Mode`: (Currently disabled)
- `Button visibility`: whether an icon/button is displayed for mobile, desktop, or both
- `Icon url`: (Optional) the icon that is displayed on the ability's button.
