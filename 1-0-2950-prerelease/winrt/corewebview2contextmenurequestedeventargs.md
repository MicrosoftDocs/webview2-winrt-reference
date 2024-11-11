---
title: CoreWebView2ContextMenuRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/11/2024
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ContextMenuRequestedEventArgs
---

# runtimeClass CoreWebView2ContextMenuRequestedEventArgs



## Summary

Members|Description
--|--
[ContextMenuTarget](#contextmenutarget) | 
[Handled](#handled) | 
[Location](#location) | 
[MenuItems](#menuitems) | 
[SelectedCommandId](#selectedcommandid) | 
[GetDeferral](#getdeferral) | 

## Properties

### ContextMenuTarget

> readonly  [CoreWebView2ContextMenuTarget](corewebview2contextmenutarget.md) ContextMenuTarget

### Handled

>  bool Handled

### Location

> readonly  [Point](/uwp/api/Windows.Foundation.Point) Location

### MenuItems

> readonly  [`IVector`](/uwp/api/Windows.Foundation.Collections.IVector-1)&lt;[CoreWebView2ContextMenuItem](corewebview2contextmenuitem.md)&gt; MenuItems

### SelectedCommandId

>  int SelectedCommandId



## Methods

### GetDeferral

> [Deferral](/uwp/api/Windows.Foundation.Deferral) GetDeferral()






## Referenced by

- [CoreWebView2](corewebview2.md)
