---
title: CoreWebView2ContextMenuItem
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/01/2024
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ContextMenuItem
---

# runtimeClass CoreWebView2ContextMenuItem



## Summary

Members|Description
--|--
[Children](#children) | 
[CommandId](#commandid) | 
[Icon](#icon) | 
[IsChecked](#ischecked) | 
[IsEnabled](#isenabled) | 
[Kind](#kind) | 
[Label](#label) | 
[Name](#name) | 
[ShortcutKeyDescription](#shortcutkeydescription) | 
[CustomItemSelected](#customitemselected) | 

## Properties

### Children

> readonly  [`IVector`](/uwp/api/Windows.Foundation.Collections.IVector-1)&lt;[CoreWebView2ContextMenuItem](corewebview2contextmenuitem.md)&gt; Children

### CommandId

> readonly  int CommandId

### Icon

> readonly  [IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) Icon

### IsChecked

>  bool IsChecked

### IsEnabled

>  bool IsEnabled

### Kind

> readonly  [CoreWebView2ContextMenuItemKind](corewebview2contextmenuitemkind.md) Kind

### Label

> readonly  string Label

### Name

> readonly  string Name

### ShortcutKeyDescription

> readonly  string ShortcutKeyDescription




## Events

### CustomItemSelected

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2ContextMenuItem](corewebview2contextmenuitem.md), Object&gt;



## Referenced by

- [CoreWebView2Environment](corewebview2environment.md)
