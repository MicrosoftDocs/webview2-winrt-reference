---
title: CoreWebView2FrameKind
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/13/2025
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2FrameKind
---

# enum CoreWebView2FrameKind

Specifies the frame kind used in [CoreWebView2FrameInfo](corewebview2frameinfo.md).

| Name |  Value | Description |
|--|--|--|
|`Unknown` | 0x0  |  Indicates that the frame is an unknown type frame. We may extend this enum type to identify more frame kinds in the future. For example, if portal frame which current in experimental phase gets finalized, we may extend this to include a new frame kind `COREWEBVIEW2_FRAME_KIND_PORTAL`.|
|`MainFrame` | 0x1  |  Indicates that the frame is a primary main frame([CoreWebView2](corewebview2.md)).|
|`Iframe` | 0x2  |  Indicates that the frame is an iframe.|
|`Embed` | 0x3  |  Indicates that the frame is an [embed](https://developer.mozilla.org/docs/Web/HTML/Element/embed) element.|
|`Object` | 0x4  |  Indicates that the frame is an [object](https://developer.mozilla.org/docs/Web/HTML/Element/object) element.|


## Referenced by

- [CoreWebView2FrameInfo](corewebview2frameinfo.md)
