# Dialogues

In the 'Dialogues' section of the UI tab, you can customize how dialogues are rendered in your game. Currently, you can customize a single dialogue. Support for multiple dialogue views will be added in the future.

To customize the dialogue, you can add custom CSS and HTML. You can preview your changes by pressing "Save and Preview" using content from your own dialogues. The syntax with {{double brackets}} is Handlebars, which is used for dynamic content.

### The following variables are available for use:

| Name                      | Type    | Description                                                |
|---------------------------|---------|------------------------------------------------------------|
| dialogue.dialogueTitle    | String  | Title value of the dialogue                                |
| dialogue.message          | String  | HTML message for the dialogue                              |
| dialogue.image            | String  | URL of the image for the dialogue                          |
| dialogue.options          | Object  | List of options (each option is an object)                 |
| dialogue.options[index].name   | String  | Name of the option                                         |
| dialogue.areOptionsRendered | Boolean | Utility variable that returns true if options are rendered, else false |

### Recommended classes/IDs:

- `#modd-dialogue-message`: HTML ID used for typing effect functionality
- `.dialogue-option`: HTML class used for determining click on option

### Commands & Variables:

- Breaking a single dialogue into multiple pages can be achieved by adding a break like `%br%`.
- Displaying global variables can be done by wrapping them in the $ symbol (e.g., $varName$).

