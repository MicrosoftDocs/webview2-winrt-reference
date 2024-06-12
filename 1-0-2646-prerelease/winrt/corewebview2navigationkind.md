---
description: Specifies the navigation kind of each navigation.
title: CoreWebView2NavigationKind
ms.date: 06/19/2024
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2NavigationKind
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- Microsoft.Web.WebView2.Core.CoreWebView2NavigationKind
---

# CoreWebView2NavigationKind Enum

Specifies the navigation kind of each navigation.

| Name |  Value | Description |
|--|--|--|
|`Reload` | 0x0  |  A navigation caused by CoreWebView2.Reload(), location.reload(), the end user using F5 or other UX, or other reload mechanisms to reload the current document without modifying the navigation history.|
|`BackOrForward` | 0x1  |  A navigation back or forward to a different entry in the session navigation history, like via CoreWebView2.Back(), location.back(), the end user pressing Alt+Left or other UX, or other mechanisms to navigate back or forward in the current session navigation history.|
|`NewDocument` | 0x2  |  A navigation to another document, which can be caused by CoreWebView2.Navigate(),window.location.href = ..., or other WebView2 or DOM APIs that navigate to a new URI.|


## Referenced by

- [CoreWebView2NavigationStartingEventArgs](corewebview2navigationstartingeventargs.md)
