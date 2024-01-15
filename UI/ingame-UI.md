# Custom in-game user interface

Moddio offers capabilities for creating custom UI elements, registering clicks on those elements and updating their content. This enables creators to craft responsive, dynamic game UI that suits the needs of their creation. To build good custom user interfaces, you will need to make use of HTML and CSS. 

It can be used for:
- buttons that trigger actions in game
- health bars that display the current health of an enemy
- stat display modals
- lots of other graphical user interface

To create custom in-game UI, navigate to the UI workspace and start editing the `In-Game UI`. You can add any type of HTML elements here, they will be wrapped in a full-screen div with the CSS ID `custom-ingame-ui-container` that overlays the game. By default, this container is not clickable (css: `pointer-events: none`) while all elements inside of it are (css: `pointer-events: auto`). To override this and achieve non-interactible UI, add `pointer-events: none` to the element (this is use).

The default in-game UI (chat, attributes, item UI) can be edited in the `Default In-Game UI` view, there you can customize the design of individual elements like inventory, leaderboard and overlay texts.

The following script actions and triggers make it possible to have the UI and game interact:

- Trigger: [**"when a player clicks on UI HTML element"**](https://www.modd.io/docs/triggers/htmlUiClick), passes **triggeringElementId** and **triggeringPlayer**:
    
    Any UI element that is assigned the class “.trigger” will run scripts that contain this specific trigger when the element is clicked. **triggeringElementId** is a string that contains the ID of the HTML element that has been clicked, **triggeringPlayer** contains the player that has performed the clicking action.
    
- Action: [**"show/hide UI element with ID (*string*) for (*player*)"**](https://www.modd.io/docs/functions/showUiElementForPlayer):
    
    These two actions allow the creator to customize which UI elements are visible to a player at any given time. The **show** action sets the element’s css attribute for ‘display’ to its initial value (see [jQuery .show()](https://api.jquery.com/show/) function) while the **hide** action sets the ‘display’ value to ‘none’.
    
- Action: [**"set innerHTML of UI element with ID (*string*) for (*player*) to (string)"**](https://www.modd.io/docs/functions/setUIElementHtml):
    
    Useful for changing the content of any UI element to any HTML of your choice. Works the same way as the .setInnerHTML javascript function does. You will need to provide a string that contains the HTML you want to place inside the element as well as the ID of the HTML element you want to modify. You can [concatenate](https://www.modd.io/docs/variables/concat) strings achieve create complex HTML.