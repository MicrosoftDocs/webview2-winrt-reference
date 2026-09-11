---
description: Specifies the scope that originated a diagnostic event.
title: CoreWebView2DiagnosticScope
ms.date: 09/03/2026
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2DiagnosticScope
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2DiagnosticScope
---

# CoreWebView2DiagnosticScope Enum

Specifies the scope that originated a diagnostic event.


| Name |  Value | Description |
|--|--|--|
|`Webview` | 0x0  |  The diagnostic signal originated from a specific WebView instance.
|
|`Profile` | 0x1  |  The diagnostic signal originated from a profile but is not tied to a specific WebView.
|
|`Environment` | 0x2  |  The diagnostic signal originated from the environment, for example a browser-wide event that affects all WebViews.
|


## Referenced by

- [CoreWebView2DiagnosticReceivedEventArgs](corewebview2diagnosticreceivedeventargs.md)
