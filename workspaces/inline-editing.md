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
There is a magical feeling so right~ ♪, huhh, as you can see, the multi-nested object is getting flat, I mean u can edit every slots at same time, no need to click to go deep the nested object, especially useful for editing those numbers.

You can copy or paste here freely, enjoy xD.

---

## "Hello World" Example
To start with a classic "hello world" example, you can choose the <code>send chat message</code> action from the dropdown menu in the script editor. Change it to inline editing mode and type "hello world" within quotes. You can also use single quotes if you need to include double quotes within the string. For example, 'once upon a time, someone said: "hello world"'.

Inline editing is particularly useful when concatenating strings with other strings or numbers. For instance, you can try typing the following code:
![sendChatMessage](../img/inline-editing/helloWorld.png)

And for <code>string</code>, it's very useful to use inline-editing when u want to concat the <code>string</code> with <code>string</code> or <code>number</code>

> Try type

```js
"a random number = " + randNumber(0, 5);
```

> Tips  
 Inline-editing will auto handle <code>string</code> + <code>number</code>, if the addition equation contains the <code>string</code>, the output will be <code>string</code>, and <code>number</code> + <code>number</code> will be concat as <code>string</code>

```js
1 + 1 + "hello" // "11hello"
(1 + 1) + "hello"; // "2hello"
```

## Action aliases
> In inline-editing, we have many action aliases to simplified function calling, here is the table  
no worries! the complete suggestions will help you, no need to remember these aliases

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

You can use these aliases directly, like pos(2, 5), created a position

## Method & Property
> do you know the method chaining?  
> it's something that you can call the functions one by one like in a chain
```js
pos(5, 6).x.abs // equals to abs(getXCoordinate(xyCoordinate(5, 6))), seems much better, right?
```

Yes, the inline-editing can help you do this thing, you only need to connect them one by one  
You may noticed that some properties have same names
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

## Attr & Var
you can use <code>someEntity.some_var</code> to get the var  
<code>someEntity.$some_attr</code> to get the attr

```js
// you need to define these attr or var first in entity editor
thisEntity.deathCount
thisEntity.$health
```

## If statement

In inline editing, you can use various operators for conditional statements. Here are a few examples:

- **&&** (and): pos(0, 1).y > 1 && thisEntity.$health != 10
- **||** (or): pos(0, 1).y > 1 || thisEntity.$health == 10
- **!=** (not equal): 1 != 2
- **==** (equal): 1 == 1
- **>, <, >=, <=**: pos(0, 1).y > 1 && thisEntity.$health <= 10

## Playground
you can always play in playground first, enjoy it.  
[playground](https://moddio.github.io/script-editor/?path=/docs/textscripteditor--docs)
<iframe style="height: 40rem" src = "https://moddio.github.io/script-editor/?path=/docs/textscripteditor--docs" >
</iframe>

## Examples
