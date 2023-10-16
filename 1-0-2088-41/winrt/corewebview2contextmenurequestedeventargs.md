---
description: 
title: CoreWebView2ContextMenuRequestedEventArgs
ms.date: 10/16/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ContextMenuRequestedEventArgs
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuRequestedEventArgs
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuRequestedEventArgs.ContextMenuTarget
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuRequestedEventArgs.Handled
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuRequestedEventArgs.Location
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuRequestedEventArgs.MenuItems
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuRequestedEventArgs.SelectedCommandId
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuRequestedEventArgs.GetDeferral
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuRequestedEventArgs.get_ContextMenuTarget
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuRequestedEventArgs.get_Handled
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuRequestedEventArgs.get_Location
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuRequestedEventArgs.get_MenuItems
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuRequestedEventArgs.get_SelectedCommandId
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuRequestedEventArgs.put_Handled
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuRequestedEventArgs.put_SelectedCommandId
---

# CoreWebView2ContextMenuRequestedEventArgs Class



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
