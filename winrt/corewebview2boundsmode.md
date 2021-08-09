---
title: CoreWebView2BoundsMode
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/10/2021
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2BoundsMode
---

# enum CoreWebView2BoundsMode

Mode for how the [CoreWebView2Controller.Bounds](corewebview2controller.md#bounds) property is interpreted in relation to the [CoreWebView2Controller.RasterizationScale](corewebview2controller.md#rasterizationscale) property.

| Name |  Value | Description |
|--|--|--|
|`UseRawPixels` | 0x0  |  [CoreWebView2Controller.Bounds](corewebview2controller.md#bounds) property represents raw pixels. Physical size of WebView is not impacted by [CoreWebView2Controller.RasterizationScale](corewebview2controller.md#rasterizationscale)|
|`UseRasterizationScale` | 0x1  |  [CoreWebView2Controller.Bounds](corewebview2controller.md#bounds) property represents logical pixels and the [CoreWebView2Controller.RasterizationScale](corewebview2controller.md#rasterizationscale) property is used to get the physical size of the WebView.|


## Referenced by

- [CoreWebView2Controller](corewebview2controller.md)
