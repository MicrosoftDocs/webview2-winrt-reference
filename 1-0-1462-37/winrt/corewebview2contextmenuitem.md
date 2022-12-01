---
description: Represents a context menu item of a context menu displayed by WebView.
title: CoreWebView2ContextMenuItem
ms.date: 12/05/2022
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ContextMenuItem
---

# CoreWebView2ContextMenuItem Class



Represents a context menu item of a context menu displayed by WebView.

## Summary

Members|Description
--|--
[Children](#children) | Gets the list of children menu items if the kind is [CoreWebView2ContextMenuItemKind](corewebview2contextmenuitemkind.md).Submenu.
[CommandId](#commandid) | Gets the Command ID for the CoreWebView2ContextMenuItem.
[Icon](#icon) | Gets the Icon for the CoreWebView2ContextMenuItem in PNG, Bitmap or SVG formats in the form of an IStream.
[IsChecked](#ischecked) | Gets or sets the checked property of the CoreWebView2ContextMenuItem.
[IsEnabled](#isenabled) | Gets or sets the enabled property of the CoreWebView2ContextMenuItem. Must only be used in the case of a custom context menu item.
[Kind](#kind) | Gets the kind of CoreWebView2ContextMenuItem as [CoreWebView2ContextMenuItemKind](corewebview2contextmenuitemkind.md).
[Label](#label) | Gets the localized label for the CoreWebView2ContextMenuItem. Will contain an ampersand for characters to be used as keyboard accelerator.
[Name](#name) | Gets the unlocalized name for the CoreWebView2ContextMenuItem.
[ShortcutKeyDescription](#shortcutkeydescription) | Gets the localized keyboard shortcut for this CoreWebView2ContextMenuItem.
[CustomItemSelected](#customitemselected) | CustomItemSelected event is raised when the user selects this CoreWebView2ContextMenuItem.

## Properties

### Children

> readonly  [`IVector`](/uwp/api/Windows.Foundation.Collections.IVector-1)&lt;CoreWebView2ContextMenuItem&gt; Children

Gets the list of children menu items if the kind is [CoreWebView2ContextMenuItemKind](corewebview2contextmenuitemkind.md).Submenu.
If the kind is not [CoreWebView2ContextMenuItemKind](corewebview2contextmenuitemkind.md).Submenu, will return `null`.

### CommandId

> readonly  int CommandId

Gets the Command ID for the CoreWebView2ContextMenuItem.
Use this to report the [CoreWebView2ContextMenuRequestedEventArgs.SelectedCommandId](corewebview2contextmenurequestedeventargs.md#selectedcommandid) in [CoreWebView2.ContextMenuRequested](corewebview2.md#contextmenurequested) event.

### Icon

> readonly  [IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) Icon

Gets the Icon for the CoreWebView2ContextMenuItem in PNG, Bitmap or SVG formats in the form of an IStream.
Stream will be rewound to the start of the image data before being read.

### IsChecked

>  bool IsChecked

Gets or sets the checked property of the CoreWebView2ContextMenuItem.
Must only be used for custom context menu items that are of kind [CoreWebView2ContextMenuItemKind](corewebview2contextmenuitemkind.md).CheckBox or [CoreWebView2ContextMenuItemKind](corewebview2contextmenuitemkind.md).Radio.

### IsEnabled

>  bool IsEnabled

Gets or sets the enabled property of the CoreWebView2ContextMenuItem. Must only be used in the case of a custom context menu item.
The default value for this is `true`.

### Kind

> readonly  [CoreWebView2ContextMenuItemKind](corewebview2contextmenuitemkind.md) Kind

Gets the kind of CoreWebView2ContextMenuItem as [CoreWebView2ContextMenuItemKind](corewebview2contextmenuitemkind.md).

### Label

> readonly  string Label

Gets the localized label for the CoreWebView2ContextMenuItem. Will contain an ampersand for characters to be used as keyboard accelerator.

### Name

> readonly  string Name

Gets the unlocalized name for the CoreWebView2ContextMenuItem.
Use this to distinguish between context menu item types. This will be the English label of the menu item in lower camel case. For example, the "Save as" menu item will be "saveAs". Extension menu items will be "extension", custom menu items will be "custom" and spellcheck items will be "spellCheck".
Some example context menu item names are:

- "saveAs"
- "copyImage"
- "openLinkInNewWindow"

### ShortcutKeyDescription

> readonly  string ShortcutKeyDescription

Gets the localized keyboard shortcut for this CoreWebView2ContextMenuItem.
It will be the empty string if there is no keyboard shortcut. This is text intended to be displayed to the end user to show the keyboard shortcut. For example this property is Ctrl+Shift+I for the "Inspect" CoreWebView2ContextMenuItem.




## Events

### CustomItemSelected

CustomItemSelected event is raised when the user selects this CoreWebView2ContextMenuItem.
Will only be raised for end developer created context menu items.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2ContextMenuItem, Object&gt;



## Referenced by

- [CoreWebView2Environment](corewebview2environment.md)
