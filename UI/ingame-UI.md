# UI editing

Moddio offers capabilities for creating custom UI elements, registering clicks on those elements and updating their content. This enables creators to craft responsive, dynamic game UI that suits the needs of their creation.

To create custom in-game UI, navigate to the UI workspace and start editing the “In-Game UI”. You can add any type of HTML elements here, they will be wrapped in a full-screen div that overlays the game.

The default in-game UI (chat, attributes, item UI) can not be edited in this view, but you can still customize the design of individual elements by applying custom CSS.

The following script actions and triggers make it possible to have the UI and game interact:

- Trigger: **"when a player clicks on UI HTML element"**, passes **triggeringElementId** and **triggeringPlayer:**
    
    Any UI element that is assigned the class “.trigger” will run scripts that contain this specific trigger when the element is clicked. **triggeringElementId** is a string that contains the ID of the HTML element that has been clicked, **triggeringPlayer** contains the player that has performed the clicking action
    
- Action: **"show/hide UI element with ID (*string*) for (*player*)":**
    
    These two actions allow the creator to customize which UI elements are visible to a player at any given time. The **show** action sets the element’s css attribute for ‘display’ to its initial value (see [jQuery .show()](https://api.jquery.com/show/) function) while the **hide** action sets the ‘display’ value to ‘none’.
    
- Action: **"set innerHTML of UI element with ID (*string*) for (*player*) to (string)"**
    
    Useful for changing the content of any UI element to any HTML of your choice. If you want to create complex HTML, you can concatenate strings