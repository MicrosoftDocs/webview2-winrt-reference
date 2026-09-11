---
description: Event args for the CoreWebView2DiagnosticMonitor.DiagnosticReceived event. Each instance represents a single diagnostic signal.
title: CoreWebView2DiagnosticReceivedEventArgs
ms.date: 09/03/2026
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2DiagnosticReceivedEventArgs
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2DiagnosticReceivedEventArgs
- CoreWebView2DiagnosticReceivedEventArgs.Category
- CoreWebView2DiagnosticReceivedEventArgs.DetailsAsJson
- CoreWebView2DiagnosticReceivedEventArgs.Scope
- CoreWebView2DiagnosticReceivedEventArgs.Timestamp
---

# CoreWebView2DiagnosticReceivedEventArgs Class



Event args for the [CoreWebView2DiagnosticMonitor.DiagnosticReceived](corewebview2diagnosticmonitor.md#diagnosticreceived) event. Each instance represents a single diagnostic signal.


## Summary

Members|Description
--|--
[Category](#category) | The diagnostic category that this event belongs to.
[DetailsAsJson](#detailsasjson) | Returns category-specific diagnostic data as a JSON string.
[Scope](#scope) | The scope that originated this diagnostic signal.
[Timestamp](#timestamp) | The wall-clock time at which the runtime observed this diagnostic event.

## Properties

### Category

> readonly  [CoreWebView2DiagnosticCategory](corewebview2diagnosticcategory.md) Category

The diagnostic category that this event belongs to.


### DetailsAsJson

> readonly  string DetailsAsJson

Returns category-specific diagnostic data as a JSON string.
The schema for each category is documented on the corresponding [CoreWebView2DiagnosticCategory](corewebview2diagnosticcategory.md) value. The runtime may include additional key-value pairs beyond the documented fields; consumers should ignore unknown keys.


### Scope

> readonly  [CoreWebView2DiagnosticScope](corewebview2diagnosticscope.md) Scope

The scope that originated this diagnostic signal.


### Timestamp

> readonly  int64_t Timestamp

The wall-clock time at which the runtime observed this diagnostic event.
Use this value to correlate diagnostic events with other timestamped telemetry. The value is derived from the system clock and may be affected by clock adjustments, for example NTP.







## Referenced by

- [CoreWebView2DiagnosticMonitor](corewebview2diagnosticmonitor.md)
