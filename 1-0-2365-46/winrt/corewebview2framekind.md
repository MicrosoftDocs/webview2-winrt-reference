---
description: Specifies the frame kind used in CoreWebView2FrameInfo.
title: CoreWebView2FrameKind
ms.date: 02/26/2024
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2FrameKind
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- Microsoft.Web.WebView2.Core.CoreWebView2FrameKind
---

# CoreWebView2FrameKind Enum

Specifies the frame kind used in [CoreWebView2FrameInfo](corewebview2frameinfo.md).

| Name |  Value | Description |
|--|--|--|
|`Unknown` | 0x0  |  Indicates that the frame is an unknown type frame. We may extend this enum type to identify more frame kinds in the future. For example, if portal frame which current in experimental phase gets finalized, we may extend this to include a new frame kind `COREWEBVIEW2_FRAME_KIND_PORTAL`.|
|`MainFrame` | 0x1  |  Indicates that the frame is a primary main frame([CoreWebView2](corewebview2.md)).|
|`Iframe` | 0x2  |  Indicates that the frame is an iframe.|
|`Embed` | 0x3  |  Indicates that the frame is an <see href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/embed">embed</see> element.|
|`Object` | 0x4  |  Indicates that the frame is an <see href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/object">object</see> element.|


## Referenced by

- [CoreWebView2FrameInfo](corewebview2frameinfo.md)
