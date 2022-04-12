---
description: Mode for how the CoreWebView2Controller.Bounds property is interpreted in relation to the CoreWebView2Controller.RasterizationScale property.
title: CoreWebView2BoundsMode
ms.date: 04/12/2022
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2BoundsMode
---

# CoreWebView2BoundsMode Enum

Mode for how the [CoreWebView2Controller.Bounds](corewebview2controller.md#bounds) property is interpreted in relation to the [CoreWebView2Controller.RasterizationScale](corewebview2controller.md#rasterizationscale) property.

| Name |  Value | Description |
|--|--|--|
|`UseRawPixels` | 0x0  |  [CoreWebView2Controller.Bounds](corewebview2controller.md#bounds) property represents raw pixels. Physical size of WebView is not impacted by [CoreWebView2Controller.RasterizationScale](corewebview2controller.md#rasterizationscale).|
|`UseRasterizationScale` | 0x1  |  [CoreWebView2Controller.Bounds](corewebview2controller.md#bounds) property represents logical pixels and the [CoreWebView2Controller.RasterizationScale](corewebview2controller.md#rasterizationscale) property is used to get the physical size of the WebView.|


## Referenced by

- [CoreWebView2Controller](corewebview2controller.md)
