---
title: CoreWebView2SharedBufferAccess
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2023
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2SharedBufferAccess
---

# enum CoreWebView2SharedBufferAccess

Specifies the desired access from script to [CoreWebView2SharedBuffer](corewebview2sharedbuffer.md).

| Name |  Value | Description |
|--|--|--|
|`ReadOnly` | 0x0  |  Script from web page only has read access to the shared buffer.|
|`ReadWrite` | 0x1  |  Script from web page has read and write access to the shared buffer.|


## Referenced by

- [CoreWebView2](corewebview2.md)
- [CoreWebView2Frame](corewebview2frame.md)
