---
description: Specifies the source of CoreWebView2.WebResourceRequested.
title: CoreWebView2WebResourceRequestSourceKinds
ms.date: 07/24/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2WebResourceRequestSourceKinds
---

# CoreWebView2WebResourceRequestSourceKinds Enum

Specifies the source of [CoreWebView2.WebResourceRequested](corewebview2.md#webresourcerequested).

| Name |  Value | Description |
|--|--|--|
|`None` | 0x0  |  |
|`Document` | 0x1  |  Indicates that web resource is requested from main page including dedicated workers and iframes.|
|`SharedWorker` | 0x2  |  Indicates that web resource is requested from shared worker.|
|`ServiceWorker` | 0x4  |  Indicates that web resource is requested from service worker.|
|`All` | 0xffffffff  |  Indicates that web resource is requested from any supported source.|


## Referenced by

- [CoreWebView2](corewebview2.md)
- [CoreWebView2WebResourceRequestedEventArgs](corewebview2webresourcerequestedeventargs.md)
