---
title: CoreWebView2WebResourceRequestSourceKinds
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/13/2025
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2WebResourceRequestSourceKinds
---

# enum CoreWebView2WebResourceRequestSourceKinds

Specifies the source of [CoreWebView2.WebResourceRequested](corewebview2.md#webresourcerequested).

| Name |  Value | Description |
|--|--|--|
|`None` | 0x0  |  |
|`Document` | 0x1  |  Indicates that web resource is requested from main page including dedicated workers, iframes and main script for shared workers.|
|`SharedWorker` | 0x2  |  Indicates that web resource is requested from shared worker.|
|`ServiceWorker` | 0x4  |  Indicates that web resource is requested from service worker.|
|`All` | 0xffffffff  |  Indicates that web resource is requested from any supported source.|


## Referenced by

- [CoreWebView2](corewebview2.md)
- [CoreWebView2WebResourceRequestedEventArgs](corewebview2webresourcerequestedeventargs.md)
