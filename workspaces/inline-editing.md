<table style="display: flex;justify-content: center;" id="moddioVersion">
<thead>
    <tr>
        <th>Moddio Version: 2.0.11</th>
        <th>(current)</th>
    </tr>
</thead>
<tbody></tbody>
</table>

# Inline-editing

> 🚧 Beware! inline-editing is heavily under construction and a lot of things may change.
> Please use the latest version whenever possible


If you're tired of clicking on each slot in the script editor, there's a solution for you: inline editing. You can change the editing mode in the script modal or use the shortcut <code>**ctrl+q**</code> to toggle the editing mode. This feature allows you to edit multiple slots simultaneously without having to navigate through nested objects. It's especially useful for editing numbers. You can freely copy and paste in the inline editing mode.

[inline-editing](../img/inline-editing/introduce.png)

![magic](../img/inline-editing/firstUseInline.png)  
As you can see, the nested script action is getting 'flattened' into a single code string. This allows you to edit the complete script action at once without the need to navigate deep into the nested object. It also enables copying ang pasting snippets of code freely.

---

## "Hello World" Example
To start with a classic "hello world" example, you can choose the <code>send chat message</code> action from the dropdown menu in the script editor. Switch to inline editing mode and type "hello world" within quotes. You can also use single quotes if you need to include double quotes within the string. For example, 'once upon a time, someone said: "hello world"'.

![sendChatMessage](../img/inline-editing/helloWorld.png)  

Inline editing is particularly useful when concatenating strings with other strings or numbers. For instance, you can try typing the following code:  

> Try typing

```js
"a random number = " + randNumber(0, 5);
```

> Tips  
 Inline-editing will automatically handle <code>string</code> + <code>number</code> if the addition equation contains the <code>string</code>, the output will be <code>string</code>, and <code>number</code> + <code>number</code> will be concat as <code>string</code>

```js
1 + 1 + "hello" // "11hello"
(1 + 1) + "hello"; // "2hello"
```

## Action aliases
> In inline-editing, we have many action aliases to simplify function calling, here is the table  
Don't worry! The autocomplete suggestions will help you, so there's no need to remember these aliases.

| Function Name | Alias |
| --- | --- |
| getRandomNumberBetween | randNumber |
| xyCoordinate | pos |
| dynamicRegion | region |
| mathFloor | floor |
| squareRoot | sqrt |
| getRandomItemTypeFromItemTypeGroup | randItemType |
| stringToNumber | str2num |
| getPositionY | y |
| getPositionX | x |
| getXCoordinateOfRegion | x |
| getYCoordinateOfRegion | y |
| getItemTypeOfItem | type |
| getUnitTypeOfUnit | type |
| playerTypeOfPlayer | type |
| getRandomUnitTypeFromUnitTypeGroup | type |
| undefinedValue | undefined |
| getRandomPositionInRegion | randPos |
| substringOf | slice |
| absoluteValueOfNumber | abs |
| getExponent | pow |
| numberToString | num2str |
| stringToObject | str2obj |
| objectToString | obj2Str |
| unitsFacingAngle | facingAngle |
| getCurrentAmmoOfItem | currentAmmo |
| changeDescriptionOfItem | changeDesc |
| getOwnerOfItem | owner |
| setFadingTextOfUnit | setFadingText |
| getSensorOfUnit | sensor |
| getPositionInFrontOfPosition | polarProjection |
| lastPlayedTimeOfPlayer | lastPlayedTime |
| getLastPurchasedUnit | lastPurchasedUnit |
| getLastPlayerSelectingDialogueOption | lastSelectingDialogueOption |
| getTriggeringItem | triggeringItem |
| playerCustomInput | lastPlayerInput |
| getTriggeringRegion | triggeringRegion |
| getLastOverlappingUnit | lastOverlappingUnit |
| lastPurchasedUnitTypetId | lastPurchasedUnitType |
| getTriggeringPlayer | triggeringPlayer |
| getLastOverlappedUnit | lastOverlappedUnit |
| getLastCreatedItem | lastCreatedItem |
| getLastCreatedProjectile | lastCreatedProjectile |
| getLastTouchingUnit | lastTouchingUnit |
| getLastOverlappingItem | lastOverlappingItem |
| entityLastRaycastCollisionPosition | lastRaycastCollisionPos |
| getLastCastingUnit | lastCastingUnit |
| getLastTouchedUnit | lastTouchedUnit |
| getTriggeringProjectile | triggeringProj |
| getLastCreatedUnit | lastCreatedUnit |
| getTriggeringUnit | triggeringUnit |
| getLastTouchedItem | lastTouchedItem |
| getLastTouchedProjectile | lastTouchedProj |
| getLastOverlappingProjectile | lastOverlappingProj |
| getTriggeringAttribute | triggeringAttr |
| getLastAttackedUnit | lastAttackedUnit |
| getLastAttackingUnit | lastAttackingUnit |
| getLastChatMessageSentByPlayer | lastChatMessageSent |
| getLastAttackingItem | lastAttackingItem |

You can use these aliases directly. For example, `pos(2, 5)` creates a position [2|5] just like `xyCoordinate(2, 5)` does.

## Method & Property
> Do you know about method chaining?  
> It's something that allows you to call the functions one by one like in a chain by connectiong the function calls with dots like:
```js
pos(5, 6).x.abs // equals to abs(getXCoordinate(xyCoordinate(5, 6))), seems much better, right?
```
Method chaining can help shorten long, nested chains of function calls.

Yes, the inline-editing can help you do this thing, you only need to connect them one by one.
Some properties have the same names with functions that differ based on context: 
```js
// inline-editing can handle different data type with the same name
// you don't need to use 'getPositionX' for pos, 'getXCoordinateOfRegion' for region
pos(1,1).x // 1
region(2,2,1,1).x // 2
```

here is the table of contents currently available

|x|y|type|
|---|---|---|
|region|region|item|
|pos|pos|unit|
|-|-|player|
|-|-|unitTypeGroup|

## Attributes & Variables
Use <code>someEntity.some_var</code> to get the entity variable. An autocomplete dropdown will open once you type the `.` that lists all available variables of the entity.   
Similarly, <code>someEntity.$some_attr</code> accesses the entered attribute of the entity. Once you type `.$` after an entity, autosuggest will provide you with possible attribute selections.

```js
// you need to define these attr or var first in entity editor
thisEntity.deathCount
thisEntity.$health
```
Remember: `entity.` to list **variables**, `entity.$` to list **attributes**.

## If statement

In inline editing, you can use various operators for conditional statements. Here are a few examples:

- **&&** (and): `pos(0, 1).y > 1 && thisEntity.$health != 10` resolves true if both conditions are true
- **||** (or): `pos(0, 1).y > 1 || thisEntity.$health == 10` resolves to true if either condition is true
- **!=** (not equal): `1 != 2` resolves true if the parameters do not match
- **==** (equal): `1 == 1` resolves true if the parameters match
- **>, <, >=, <=** (bigger than, smaller than, bigger or equal to, smaller or equal to): pos(0, 1).y > 1 && thisEntity.$health <= 10

## Playground
You can try inline scripting in the playground:  
[playground](https://moddio.github.io/script-editor/?path=/docs/textscripteditor--docs)
<iframe style="height: 40rem" src = "https://moddio.github.io/script-editor/?path=/docs/textscripteditor--docs" >
</iframe>

## Q&A

#### Oh no, my editor crashed! What should I do?
---
> This feature is still in beta and we're sorry that happened. The error message includes an option to save and republish your game, so you should not be losing much progress. Feel free to open an issue on [Github](https://github.com/moddio/moddio2/issues) or direct message @jiloduo (Moe'Thun) on discord. A copy of the error logs and ideally some screenshots + a description of your last action will be very helpful with fixing issues and bugs.

#### Which method is better? Default or Inline?
---
> Once you get the hang of it, inline will be faster for almost all actions. The default mode of visual scripting is a great entry point for beginners, but if you want to be an efficient game developer on Moddio, you should learn inline. 

#### How can I contribute to inline editing?
---
> For now, there are two repos of inline editing,
- [script-parser](https://github.com/moddio/script-parser)
- [script-editor](https://github.com/moddio/script-editor)
> Check the README.md to know more
