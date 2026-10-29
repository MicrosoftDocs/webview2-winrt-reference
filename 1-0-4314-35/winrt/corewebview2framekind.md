---
description: Indicates the frame type used in the CoreWebView2FrameInfo.
title: CoreWebView2FrameKind
ms.date: 10-29-2026
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2FrameKind
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2FrameKind
---

# CoreWebView2FrameKind Enum

Indicates the frame type used in the [CoreWebView2FrameInfo](corewebview2frameinfo.md).

| Name |  Value | Description |
|--|--|--|
|`Unknown` | 0x0  |  Indicates that the frame is an unknown type frame. We may extend this enum type to identify more frame kinds in the future.|
|`MainFrame` | 0x1  |  Indicates that the frame is a primary main frame ([CoreWebView2](corewebview2.md)).|
|`Iframe` | 0x2  |  Indicates that the frame is an iframe.|
|`Embed` | 0x3  |  Indicates that the frame is an embed element.|
|`Object` | 0x4  |  Indicates that the frame is an object element.|


## Referenced by

- [CoreWebView2FrameInfo](corewebview2frameinfo.md)
