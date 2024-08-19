# LibEasyMenu Documentation

## Overview

LibEasyMenu is a lightweight library designed to simplify the creation and management of dropdown menus within World of Warcraft addons. It provides a straightforward interface for constructing menus, customizing their appearance, and handling user interactions.

This library was created in response to Blizzard's removal of the built-in dropdown menu functionality from the World of Warcraft API, offering a replacement for developers who need similar capabilities.

## Installation

To integrate LibEasyMenu into your addon, place the `LibEasyMenu.lua` file within your addon's `libs` directory.

## Usage

Use the following command to access the library:

```lua
local LibEasyMenu = LibStub("LibEasyMenu-1.0")
```

## Functions

### `LibEasyMenu.Create(menuList, menuFrame, anchor, x, y, displayMode, autoHideDelay)`

Creates and displays a dropdown menu.

**Parameters:**
- `menuList`: A table of menu items, each with a `text` property.
- `menuFrame`: The frame to which the menu will be attached (optional).
- `anchor`: The anchor point for the menu (optional).
- `x`: The x offset for the menu (optional).
- `y`: The y offset for the menu (optional).
- `displayMode`: The display mode of the menu (optional, defaults to "MENU").
- `autoHideDelay`: The delay before automatically hiding the menu (optional).

### `LibEasyMenu.Initialize(frame, level, menuList)`

Initializes a dropdown menu with the given menu items. (Internal use)

**Parameters:**
- `frame`: The frame to which the menu items will be added.
- `level`: The menu level (for submenus).
- `menuList`: A table of menu items.

## Example
```lua
local myMenu = {
    { text = "Option 1" },
    { text = "Option 2" },
    { text = "Option 3" }
}
```

LibEasyMenu.Create(myMenu, nil, "TOPLEFT", 100, -100)

## Customization

To customize the appearance and behavior of menu items, you can add additional properties to the menu item table:

- `icon`: The texture path for the menu item's icon.
- `func`: A function to be called when the menu item is clicked.
- `arg1`: An optional argument to pass to the `func`.

## Additional Notes

For more complex menu structures, consider nesting menu lists within menu items to create submenus.

While this documentation provides a basic overview, it's recommended to explore additional customization options and error handling for production-ready addons.

By following these guidelines, you can effectively utilize LibEasyMenu to enhance your World of Warcraft addon with user-friendly dropdown menus.
