

## Game Editor Overview

Moddio game development is meant to be a multiplayer experience so that it's fun and collaborative to make a game.

With this editor, you'll be able to:
* Edit maps live with friends
* Work on scripts and game code in a shared environment

Features we're working on:
* Adding functionality that's missing from old sandbox

Since the editor is in active development, we suggest you **make frequent backups** of your `game.json` while working in it. To make a backup, click **Editor**, then select 'Export JSON'. You can import the JSON at any time, also through the Editor section.

### General Usage:

The top bar allows you to switch between **4 different workspaces**:

*   Map Editor: You can edit the map here. You have access to tools, a layer selector and a tile picker.

*   Entities: Allows you to inspect and edit scripts. Most changes here require a republish to take effect.

*   Moderate: Use this workspace to ban/kick/mute players.

*   Debug: Allows you to inspect the games variables and performance reports.

The **Menu** dropdown in the upper left corner gives you access to the Game Settings and allows you to make a backup.

### Map Editor:

In the Map Editor workspace you'll see:

*   **Tools and Size Buttons**

    *   The **Cursor Tool** allows you to interact with any regions or entities on the map with a **Left Click**.

    *   The **Region Tool** allows you to create regions. These can be used in Scripts, such as allowing actions and events to occur within defined regions.

    *   The **Stamp Brush** acts like a brush. It allows you place your current selected tile selection on the Map with a **Left Click**.    

    *   The **Eraser** erases your current tile selection. It's useful for removing tiles.

    *   The **1x1** and **2x2** selections allow you to change the size of your brush.

*   **Layer Toggle** is under the tools. Layers are ordered from top to bottom, so Trees are always on top of Walls and the Floor layers.  You can switch layers by clicking on the layer of your choice. You are always working on the selected layer and any changes using the tools will occur on that layer.

*   **Tile Picker** is in the bottom corner. You can toggle the Tile Picker on or off by clicking on **palette** or pressing the **tab** key. When expanded, you can select tiles within the palette to place on the map.



**Right click** on the map will copy the tiles your cursor is currently on top of, including any empty tiles.

