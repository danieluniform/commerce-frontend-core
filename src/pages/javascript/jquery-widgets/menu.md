---
title: Menu widget | Commerce Frontend Development
description: Learn how to initialize and configure the Adobe Commerce and Magento Open Source Menu widget.
---

# Menu widget

The menu widget is a customized [jQuery UI Menu widget](http://api.jqueryui.com/menu/). Menu extends the default functionality with the following:

-  expanding all layers of the menu tree past the second layer
-  declaring a responsive menu
-  setting hover delay

The menu widget source is [lib/web/mage/menu.js].

## Initialize

For information about how to initialize a widget in a JS component or `.phtml` template, see the [Initialize JavaScript] topic.

## Options

Menu widget options mostly coincide with the options of the jQuery UI Menu widget, with addition of some custom options.

### `delay`

Set the delay length of opening submenu.

**Type**: Number

**Default value**: `300`

### `showDelay`

Set the delay length of showing menu. Used in `toggle` method of the widget.

**Type**: Number

**Default value**: `42`

### `hideDelay`

Set the delay length of closing menu. Used in `toggle` method of the widget.

**Type**: Number

**Default value**: `300`

### `responsive`

Setting the default responsive handler for the navigation widget.

**Type**: Boolean.

**Default value**: `false`

### `mediaBreakpoint`

Sets the width of user’s window in pixels for which the menu switches between mobile view and desktop view.

**Type**: String.

**Default value**: `(max-width: 768px)`

### `expanded`

Display top level navigational items in mobile menu or all items.

**Type**: Boolean.

**Default value**: `false`

## Methods and Events

The menu widget has all default [jQuery UI menu widget] methods and events,
plus a couple more.

### Additional available methods

### `toggle()`

Toggles website's menu opened state.

### `isExpanded()`

Add class for expanded option.

<InlineAlert variant="info" slots="text" />

The following methods from [jQuery UI menu widget] were adjusted in scope of the widget: `expand(event)` and `select(event)`.

[lib/web/mage/menu.js]: https://github.com/magento/magento2/blob/2.4/lib/web/mage/menu.js
[Initialize JavaScript]: ../init.md
[jQuery UI menu widget]: http://api.jqueryui.com/menu/

## Code Sample

The following example shows how to initialize the widget and pass options during
the initialization ([declarative notation] using the `data-mage-init` attribute).

[declarative notation]: ../init.md#use-the-data-mage-init-attribute

```html
<nav class="navigation" data-action="navigation">
    <ul id="menu" data-mage-init='{"menu":{"responsive":true, "expanded":true, "delay": 200, "position":{"my":"left top","at":"left+10 top+30"}}}'>
        <li class="level0 level-top ui-menu-item">Toys</li>
        <li class="level0 level-top parent ui-menu-item">Electronics
            <ul class="level0 submenu ui-menu ui-widget ui-widget-content ui-corner-all">
                <li class="ui-menu-item"><a href="#">Home Entertainment</a></li>
                <li class="ui-menu-item"><a href="#">Routers</a></li>
            </ul>
        </li>
        <li class="level0 level-top ui-menu-item">Music
            <ul class="level0 submenu ui-menu ui-widget ui-widget-content ui-corner-all">
                <li class="ui-menu-item">
                    <a href="#">Alternative</a>
                </li>
                <li class="ui-menu-item">
                    <a href="#">Classic</a>
                </li>
            </ul>
        </li>
    </ul>
</nav>
```

### Result

The result is a menu with the child items, as shown here:

![Menu Widget](../../_images/javascript/menu-widget-result.png)
