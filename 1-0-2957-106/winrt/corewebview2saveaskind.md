---
title: CoreWebView2SaveAsKind
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/13/2025
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2SaveAsKind
---

# enum CoreWebView2SaveAsKind

Specifies [CoreWebView2SaveAsUIShowingEventArgs.Kind](corewebview2saveasuishowingeventargs.md#kind) selection options.
For HTML documents, we support 3 Save As kinds: HtmlOnly, SingleFile and Complete. For non-HTML documents, you must use Default. MIME types of `text/html` and `application/xhtml+xml` are considered HTML documents.

| Name |  Value | Description |
|--|--|--|
|`Default` | 0x0  |  Default kind to save non-HTML content. If this kind is selected for an HTML page, the behavior is the same as the `HtmlOnly` kind.|
|`HtmlOnly` | 0x1  |  Save the page as HTML. Only the top-level document is saved, excluding subresources.|
|`SingleFile` | 0x2  |  Save the page as [MHTML](https://en.wikipedia.org/wiki/MHTML).|
|`Complete` | 0x3  |  Save the page as HTML and download the page-related source files (for example: CSS, JavaScript, images, etc.) in a directory with the same filename prefix.
|


## Referenced by

- [CoreWebView2SaveAsUIShowingEventArgs](corewebview2saveasuishowingeventargs.md)
