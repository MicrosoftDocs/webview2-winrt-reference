---
description: Specifies the web resource request contexts.
title: CoreWebView2WebResourceContext
ms.date: 04/29/2025
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2WebResourceContext
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2WebResourceContext
---

# CoreWebView2WebResourceContext Enum

Specifies the web resource request contexts.

| Name |  Value | Description |
|--|--|--|
|`All` | 0x0  |  Specifies all resources.|
|`Document` | 0x1  |  Specifies a document resources.|
|`Stylesheet` | 0x2  |  Specifies a CSS resources.|
|`Image` | 0x3  |  Specifies an image resources.|
|`Media` | 0x4  |  Specifies another media resource such as a video.|
|`Font` | 0x5  |  Specifies a font resource.|
|`Script` | 0x6  |  Specifies a script resource.|
|`XmlHttpRequest` | 0x7  |  Specifies an XML HTTP request, Fetch and EventSource HTTP communication.|
|`Fetch` | 0x8  |  Specifies a Fetch API communication.

Note that this isn't working. Fetch API requests are fired as a part
of COREWEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST.|
|`TextTrack` | 0x9  |  Specifies a TextTrack resource.|
|`EventSource` | 0xa  |  Specifies an EventSource API communication.

Note that this isn't working. EventSource API requests are fired as a part
of COREWEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST.|
|`Websocket` | 0xb  |  Specifies a WebSocket API communication.|
|`Manifest` | 0xc  |  Specifies a Web App Manifest.|
|`SignedExchange` | 0xd  |  Specifies a Signed HTTP Exchange.|
|`Ping` | 0xe  |  Specifies a Ping request.|
|`CspViolationReport` | 0xf  |  Specifies a CSP Violation Report.|
|`Other` | 0x10  |  Specifies an other resource.|


## Referenced by

- [CoreWebView2](corewebview2.md)
- [CoreWebView2WebResourceRequestedEventArgs](corewebview2webresourcerequestedeventargs.md)
