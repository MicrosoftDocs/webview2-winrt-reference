---
description: This enum contains values representing possible regions a given point lies within.
title: CoreWebView2NonClientRegionKind
ms.date: 10/29/2026
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2NonClientRegionKind
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2NonClientRegionKind
---

# CoreWebView2NonClientRegionKind Enum

This enum contains values representing possible regions a given point lies within.
The values of this enum align with the matching WM_NCHITTEST* window message return values.

| Name |  Value | Description |
|--|--|--|
|`Nowhere` | 0x0  |  A hit test region out of bounds of the WebView2. This has the same value as the Win32 HTNOWHERE|
|`Client` | 0x1  |  A hit test region in the WebView2 which does not have the CSS style `-webkit-app-region: drag` set. This is normal web content that should not be considered part of the app window's title bar. This has the same value as the Win32 HTCLIENT constant.|
|`Caption` | 0x2  |  A hit test region in the WebView2 which has the CSS style `-webkit-app-region: drag` set. Web content should use this CSS style to identify regions that should be treated like the app window's title bar. This has the same value as the Win32 HTCAPTION constant.|
|`Minimize` | 0x8  |  A hit test region in the Webview2 which corresponds to the minimize window control button.|
|`Maximize` | 0x9  |  A hit test region in the Webview2 which corresponds to the maximize window control button.|
|`Close` | 0x14  |  A hit test region in the Webview2 which corresponds to the close window control button.|


## Referenced by

- [CoreWebView2CompositionController](corewebview2compositioncontroller.md)
- [CoreWebView2NonClientRegionChangedEventArgs](corewebview2nonclientregionchangedeventargs.md)
