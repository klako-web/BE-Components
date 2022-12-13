# Endless Context Menu

---
>**This component has not been released yet!**
---

This is the documentation for the UI component ***Endless Context Menu*** for the [Backendless Full Stack Visual App Development Platform](https://backendless.com).

<center>

![Icon](./assets/C-Menu.jpg)

</center>

## Use Cases
For desktop web applications, define context menus which appear on right-mouse-click. On one page, multiple menus can be defined by linking one menu to a UI element. Clicking on a menu item triggers an event handler where you can code the respective actions. Context menus can have a two-level hierarchical structure.

![Sample](./assets/sample.png)

## General usage
Place the component within a Block-UI-component which shall show the context menu on right-mouse-click.

## Properties

### Items
A list (= array) of menu item objects. The list contains objects each representing a menu item with its properties. Separator lines are represented by the string ``"hr"``. Items can be defined by directly assigning a JSON object to the ``Items``-property, or by data binding. The default value for the ``Items``-property provides an example of how to define a JSON object:
```json
[{
  "action": "copy",
  "label": "Copy",
  "iconClass": "material-icons-round",
  "iconName": "content_copy"
},
  {
    "action": "paste",
    "label": "Paste",
    "iconClass": "material-icons-round",
    "iconName": "content_paste"
  },
  "hr",
  {
    "action": "submenu",
    "label": "more ...",
    "submenu":
    [{
      "action": "subaction1",
      "label": "Sub-Action 1"
    },
      {
        "action": "subaction2",
        "label": "Sub-Action 2"
      }]
  }]
```
The following properties can be used to define a menu item object:
- ``action``: an Id which identifies the action to be performed when clicking on the menu item.
- ``label``: the text which will be shown to the user. If you support multi-lingual applications, ``action`` will identify the action to be performed, while ``label`` will vary according to the actual language.
- ``iconClass``: (optional) the name of the CSS class defining an icon set. Backendless per default includes the icon class ``material-icons-round``.
- ``iconName``: (optional) the name of an icon to be displayed left to the icon label. Names of material icons can be looked-up at https://fonts.google.com/icons?icon.style=Rounded&icon.set=Material+Icons. 
- ``submenu``: (optional) must be followed by another list (array) of menu items representing the submenu. Only one level of submenus are supported (no submenus of submenus).

If you want to define a menu programmatically, then use data binding for the ``Items``-property. As an example, assume the ``Items``-property is bound to the property ``menuItems`` of ``Page Data``. The menu can then be defined, for instance, in the ``On Page Enter`` handler:

![Define Menu](./assets/defineMenu.png)

### Close On Click
If checked (default), the menu is closed when clicking on a menu entry (except for opening a submenu).

### Show Up Duration
The duration in milliseconds used for animating the context menu. Defaults to 200 ms.

<br>

## Actions
None.

<br>

## Events

### On Items Selected
This event is raised, if a user clicks on a menu item. The handler receives the context block ``item`` with the properties ``action`` and ``label``.

![Define Menu](./assets/onItemSelected.png)

### On Error
Errors which occurr upon context menu creation, are communicated asynchroneously via this event handler. You can use this handler to log errors to the browser's developer console, or to log them with the Backendless logging API.

![Error handling](./assets/errorHandling.png)

The following pre-defined errors can be raised:

| Code  |  Message                            |
| ----- | ----------------------------------- |
| 101   | Menu definition variable must be a list (array) of objects |
| 102   | Menu item action and label must be specified |
| 103   | Submenu definition must be a list (array) of objects |
| 104   | Menu item definition must be either an object or the string 'hr' |

<br>

## Styles
Create a theme extension and change any of the following less-variables (default settings as indicated):

```css
@el-context-menu-background: @appBackgroundColor;
@el-context-menu-border: 1px solid lightGrey;
@el-context-menu-boxShadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
@el-context-menu-fontSize: 0.85em;
@el-context-menu-hoverBackground: lightGrey;
@el-context-menu-separatorColor: lightGrey;
```

<br>

## Support 
You can [open an issue](https://github.com/klako-web/Endless-Components/issues/new) and assign the label ``contextMenu``.

<br>

## Reused libraries and components
This product includes the following external code libraries/components, which are not owned by the authors of ***Endless Context Menu***:

- [vanilla-context-menu](https://github.com/GeorgianStan/vanilla-context-menu). Licensed under the [MIT License](https://github.com/GeorgianStan/vanilla-context-menu/blob/master/LICENSE).
