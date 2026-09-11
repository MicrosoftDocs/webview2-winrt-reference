---
description: Specifies the category of diagnostic event. Each value defines its own JSON schemas for the filter accepted by CoreWebView2DiagnosticMonitor.SetDiagnosticFilter and for the details returned by CoreWebView2DiagnosticReceivedEventArgs.DetailsAsJson.
title: CoreWebView2DiagnosticCategory
ms.date: 09/03/2026
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2DiagnosticCategory
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2DiagnosticCategory
---

# CoreWebView2DiagnosticCategory Enum

Specifies the category of diagnostic event. Each value defines its own JSON schemas for the filter accepted by [CoreWebView2DiagnosticMonitor.SetDiagnosticFilter](corewebview2diagnosticmonitor.md#setdiagnosticfilter) and for the details returned by [CoreWebView2DiagnosticReceivedEventArgs.DetailsAsJson](corewebview2diagnosticreceivedeventargs.md#detailsasjson).


| Name |  Value | Description |
|--|--|--|
|`NetworkRequest` | 0x0  |  Network request lifecycle signal. Fires once per network request issued by any CoreWebView2 created from this environment, after the request completes - including top-level navigations, sub-resource loads, fetch/XHR, dedicated and shared worker requests, and service-worker requests associated with one of those WebViews. Does not include requests from other host applications sharing the same user data folder, nor CSP violation reports.
The details JSON returned by [CoreWebView2DiagnosticReceivedEventArgs.DetailsAsJson](corewebview2diagnosticreceivedeventargs.md#detailsasjson) for this category includes `errorCode` (the Chromium net error code, 0 means success), `statusCode` (the HTTP response status code), `httpMethod`, `elapsedTime` (milliseconds), `scheme`, and `uri`. The runtime may include additional key-value pairs beyond those listed; consumers should ignore unknown keys.
|


## Referenced by

- [CoreWebView2DiagnosticMonitor](corewebview2diagnosticmonitor.md)
- [CoreWebView2DiagnosticReceivedEventArgs](corewebview2diagnosticreceivedeventargs.md)
