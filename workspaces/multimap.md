# Multi-Map

Multi-Map is a Moddio feature that enables users to derive Map Games from existing World Games.

#### What is a World Game?

World Game is a game whose data can be used by a Map Game. Any game can become a World Game by enabling the "World Game" setting in its configuration.
![alt text](/img/multi-map/field-setting.png)

#### What is a Map Game?

A Map Game is created from a World Game. It inherits all logic from the World Game while allowing creators to add custom map-related logic. World Game data is read-only in a Map Game, ensuring it can be referenced but not modified.
![alt text](/img/multi-map/example-maplist.png)

The attached image illustrates the Map Game editor. Map creators have access to a read-only World section and a Map section where they can add map-specific logic.

## World Game Temper Prevention

Temper Prevention safeguards player data (attributes, variables, units, and unit-owned items)  by preventing accidental changes introduced by map creators.

The engine enforces the following restrictions when running a Map Game:

- World Game Scripts: Execution of World Game scripts is prohibited when triggered by:
    - Action: run script
    - Keybinds
    - Abilities
    - Dialogues
- Modification of World Entity Data: Direct updates to World entity attributes, variables, and inventories:
    - action: set entity attribute
    - action: set player attribute
    - action: set entity variable
    - action: set player variable

- World-Scoped Item Types: Creation of item types containing World attributes and variables is disallowed.
     - action: create item

- Unit Creation and Assignment: Map scripts cannot create or assign units to players. This restriction affects actions like:
    - action: create unit at position/with dimension
    - action: assign player to player type

- Shop Manipulation:  The addition of World items and World units to map shops is prevented.

Map scripts always run after world scripts.
