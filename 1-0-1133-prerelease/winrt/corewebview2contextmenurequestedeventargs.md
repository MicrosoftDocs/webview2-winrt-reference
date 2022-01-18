---
description: Event args for the CoreWebView2.ContextMenuRequested event.
title: CoreWebView2ContextMenuRequestedEventArgs
ms.date: 01/18/2022
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ContextMenuRequestedEventArgs
---

# CoreWebView2ContextMenuRequestedEventArgs Class



Event args for the [CoreWebView2.ContextMenuRequested](corewebview2.md#contextmenurequested) event.
Will contain the selection information and a collection of all of the default context menu items that the WebView would show. Allows the app to draw its own context menu or add/remove from the default context menu.

## Summary

Members|Description
--|--
[ContextMenuTarget](#contextmenutarget) | Gets the target information associated with the requested context menu.
[Handled](#handled) | Gets or sets whether the [CoreWebView2.ContextMenuRequested](corewebview2.md#contextmenurequested) event is handled by host after the event handler completes or after the deferral is completed if there is a taken Deferral. If Handled is set to `true` then WebView2 will not display a context menu and will instead use the [CoreWebView2ContextMenuRequestedEventArgs.SelectedCommandId](corewebview2contextmenurequestedeventargs.md#selectedcommandid) property to indicate which, if any, context menu item to invoke.
[Location](#location) | Gets the coordinates where the context menu request occured in relation to the upper left corner of the WebView bounds.
[MenuItems](#menuitems) | Gets the collection of [CoreWebView2ContextMenuItem](corewebview2contextmenuitem.md) objects.
[SelectedCommandId](#selectedcommandid) | Gets or sets the selected command for the WebView to execute. The value is obtained via the [CoreWebView2ContextMenuItem.CommandId](corewebview2contextmenuitem.md#commandid) property.
[GetDeferral](#getdeferral) | Returns a Deferral object.

## Properties

### ContextMenuTarget

> readonly  [CoreWebView2ContextMenuTarget](corewebview2contextmenutarget.md) ContextMenuTarget

Gets the target information associated with the requested context menu.

### Handled

>  bool Handled

Gets or sets whether the [CoreWebView2.ContextMenuRequested](corewebview2.md#contextmenurequested) event is handled by host after the event handler completes or after the deferral is completed if there is a taken Deferral. If Handled is set to `true` then WebView2 will not display a context menu and will instead use the [CoreWebView2ContextMenuRequestedEventArgs.SelectedCommandId](corewebview2contextmenurequestedeventargs.md#selectedcommandid) property to indicate which, if any, context menu item to invoke.
If Handled is set to `true` then WebView2 will not display a context menu and will instead use the [CoreWebView2ContextMenuRequestedEventArgs.SelectedCommandId](corewebview2contextmenurequestedeventargs.md#selectedcommandid) property to indicate which, if any, context menu item to invoke. If after the event handler or deferral completes, Handled is set to `false` then WebView will display a context menu based on the contents of the [CoreWebView2ContextMenuRequestedEventArgs.MenuItems](corewebview2contextmenurequestedeventargs.md#menuitems) property. The default value is `false`.

### Location

> readonly  [Point](/uwp/api/Windows.Foundation.Point) Location

Gets the coordinates where the context menu request occured in relation to the upper left corner of the WebView bounds.

### MenuItems

> readonly  [`IVector`](/uwp/api/Windows.Foundation.Collections.IVector-1)&lt;[CoreWebView2ContextMenuItem](corewebview2contextmenuitem.md)&gt; MenuItems

Gets the collection of [CoreWebView2ContextMenuItem](corewebview2contextmenuitem.md) objects.

### SelectedCommandId

>  int SelectedCommandId

Gets or sets the selected command for the WebView to execute. The value is obtained via the [CoreWebView2ContextMenuItem.CommandId](corewebview2contextmenuitem.md#commandid) property.
This value should always be from context menu items for the relevant context menu and event arg. Attempting to mix will result in invalid outputs. The default value is -1 which means that no selected occured.



## Methods

### GetDeferral

> [Deferral](/uwp/api/Windows.Foundation.Deferral) GetDeferral()

Returns a Deferral object.
Use this operation to complete the event when the custom context menu is closed.






## Referenced by

- [CoreWebView2](corewebview2.md)
