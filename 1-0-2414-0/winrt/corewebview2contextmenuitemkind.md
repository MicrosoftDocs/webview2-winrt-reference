---
title: CoreWebView2ContextMenuItemKind
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/30/2024
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ContextMenuItemKind
---

# enum CoreWebView2ContextMenuItemKind

Specifies the menu item kind for the [CoreWebView2ContextMenuItem.Kind](corewebview2contextmenuitem.md#kind) property.

| Name |  Value | Description |
|--|--|--|
|`Command` | 0x0  |  Specifies a command menu item kind.|
|`CheckBox` | 0x1  |  Specifies a check box menu item kind. [CoreWebView2ContextMenuItem](corewebview2contextmenuitem.md) objects of this kind will need the [CoreWebView2ContextMenuItem.IsChecked](corewebview2contextmenuitem.md#ischecked) property to determine current state of the check box.|
|`Radio` | 0x2  |  Specifies a radio button menu item kind. [CoreWebView2ContextMenuItem](corewebview2contextmenuitem.md) objects of this kind will need the [CoreWebView2ContextMenuItem.IsChecked](corewebview2contextmenuitem.md#ischecked) property to determine current state of the radio button.|
|`Separator` | 0x3  |  Specifies a separator menu item kind. [CoreWebView2ContextMenuItem](corewebview2contextmenuitem.md) objects of this kind are used to signal a visual separator with no functionality.|
|`Submenu` | 0x4  |  Specifies a submenu menu item kind. [CoreWebView2ContextMenuItem](corewebview2contextmenuitem.md) objects of this kind will contain a collection of its children [CoreWebView2ContextMenuItem](corewebview2contextmenuitem.md) objects.|


## Referenced by

- [CoreWebView2ContextMenuItem](corewebview2contextmenuitem.md)
- [CoreWebView2Environment](corewebview2environment.md)
