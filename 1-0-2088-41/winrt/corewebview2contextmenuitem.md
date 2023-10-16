---
description: 
title: CoreWebView2ContextMenuItem
ms.date: 10/16/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ContextMenuItem
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuItem
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuItem.Children
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuItem.CommandId
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuItem.Icon
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuItem.IsChecked
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuItem.IsEnabled
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuItem.Kind
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuItem.Label
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuItem.Name
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuItem.ShortcutKeyDescription
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuItem.add_CustomItemSelected
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuItem.get_Children
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuItem.get_CommandId
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuItem.get_Icon
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuItem.get_IsChecked
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuItem.get_IsEnabled
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuItem.get_Kind
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuItem.get_Label
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuItem.get_Name
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuItem.get_ShortcutKeyDescription
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuItem.put_IsChecked
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuItem.put_IsEnabled
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuItem.remove_CustomItemSelected
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuItem.CustomItemSelected
---

# CoreWebView2ContextMenuItem Class



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

> readonly  [`IVector`](/uwp/api/Windows.Foundation.Collections.IVector-1)&lt;CoreWebView2ContextMenuItem&gt; Children

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

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2ContextMenuItem, Object&gt;



## Referenced by

- [CoreWebView2Environment](corewebview2environment.md)
