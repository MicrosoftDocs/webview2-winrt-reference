---
title: CoreWebView2NonClientRegionKind
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/13/2025
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2NonClientRegionKind
---

# enum CoreWebView2NonClientRegionKind

Enum which represents the kind of non-client regions.

| Name |  Value | Description |
|--|--|--|
|`Nowhere` | 0x0  |  Enum value which represents a region entirely outside the WebView2 window.|
|`Client` | 0x1  |  Enum value which represents the client area.|
|`Caption` | 0x2  |  Enum value which represents the caption area.|
|`Minimize` | 0x8  |  Enum value which represents the minimize window control button.|
|`Maximize` | 0x9  |  Enum value which represents the maximize window control button.|
|`Close` | 0x14  |  Enum value which represents the close window control button.|


## Referenced by

- [CoreWebView2CompositionController](corewebview2compositioncontroller.md)
- [CoreWebView2NonClientRegionChangedEventArgs](corewebview2nonclientregionchangedeventargs.md)
