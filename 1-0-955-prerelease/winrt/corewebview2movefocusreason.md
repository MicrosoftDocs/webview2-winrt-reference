---
description: Specifies the reason for moving focus.
title: CoreWebView2MoveFocusReason
ms.date: 08/16/2021
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2MoveFocusReason
---

# enum CoreWebView2MoveFocusReason

Specifies the reason for moving focus.

| Name |  Value | Description |
|--|--|--|
|`Programmatic` | 0x0  |  Specifies that the code is setting focus into WebView.|
|`Next` | 0x1  |  Specifies that the focus is moved due to Tab traversal forward.|
|`Previous` | 0x2  |  Specifies that the focus is moved due to Tab traversal backward.|


## Referenced by

- [CoreWebView2Controller](corewebview2controller.md)
- [CoreWebView2MoveFocusRequestedEventArgs](corewebview2movefocusrequestedeventargs.md)
