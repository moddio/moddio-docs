# Overview

Gets the ID of a tile at a position

## Usage

### Inputs

This block requires two inputs, for an X and Y coordinate. Keep in mind that the coordinates are not based on the X or Y position a unit is in, for example. Each X and Y position is not in the normal X or Y position which goes by tile width, but each tile counts as 1 X or 1 Y. The top left tile is also (0, 0), so the X and Y coordinates start at 0, not 1.

### Results

An ID is where a tile is on the game's tilemap. Here is a visual example:

![tile ID display](../img/scripting/tileID.png)

As shown, starting from the top right each tile gains 1 to its ID. This is what is given when using this function.