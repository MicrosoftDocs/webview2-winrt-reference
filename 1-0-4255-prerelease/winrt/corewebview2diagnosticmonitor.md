---
description: A diagnostic monitor that receives diagnostic signals from all layers - WebView, Profile, and Environment. Created via CoreWebView2Environment.CreateDiagnosticMonitor.
title: CoreWebView2DiagnosticMonitor
ms.date: 09/03/2026
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2DiagnosticMonitor
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2DiagnosticMonitor
- CoreWebView2DiagnosticMonitor.Close
- CoreWebView2DiagnosticMonitor.RemoveDiagnosticFilter
- CoreWebView2DiagnosticMonitor.SetDiagnosticFilter
- CoreWebView2DiagnosticMonitor.DiagnosticReceived
---

# CoreWebView2DiagnosticMonitor Class



A diagnostic monitor that receives diagnostic signals from all layers - WebView, Profile, and Environment. Created via [CoreWebView2Environment.CreateDiagnosticMonitor](corewebview2environment.md#creatediagnosticmonitor).
Each monitor has its own filters and event handlers, allowing multiple independent consumers, for example one for telemetry and one for a debug panel. The monitor is active from creation until it is released. Releasing the monitor automatically stops all events and clears all filters.


## Summary

Members|Description
--|--
[Close](#close) | 
[RemoveDiagnosticFilter](#removediagnosticfilter) | Removes the diagnostic filter for the specified category. After this call, [CoreWebView2DiagnosticMonitor.DiagnosticReceived](corewebview2diagnosticmonitor.md#diagnosticreceived) no longer fires for events in this category.
[SetDiagnosticFilter](#setdiagnosticfilter) | Sets a diagnostic filter for the specified category. After this call, [CoreWebView2DiagnosticMonitor.DiagnosticReceived](corewebview2diagnosticmonitor.md#diagnosticreceived) is raised for events in this category that match the JSON criteria.
[DiagnosticReceived](#diagnosticreceived) | Raised when a diagnostic signal passes a filter set with [CoreWebView2DiagnosticMonitor.SetDiagnosticFilter](corewebview2diagnosticmonitor.md#setdiagnosticfilter).



## Methods

### Close

> void Close()



### RemoveDiagnosticFilter

> void RemoveDiagnosticFilter([CoreWebView2DiagnosticCategory](corewebview2diagnosticcategory.md) Category)

Removes the diagnostic filter for the specified category. After this call, [CoreWebView2DiagnosticMonitor.DiagnosticReceived](corewebview2diagnosticmonitor.md#diagnosticreceived) no longer fires for events in this category.
If no filter was previously set for the category, this method is a no-op and returns `S_OK`.




### SetDiagnosticFilter

> void SetDiagnosticFilter([CoreWebView2DiagnosticCategory](corewebview2diagnosticcategory.md) Category, string jsonFilter)

Sets a diagnostic filter for the specified category. After this call, [CoreWebView2DiagnosticMonitor.DiagnosticReceived](corewebview2diagnosticmonitor.md#diagnosticreceived) is raised for events in this category that match the JSON criteria.
The filter JSON schema is category-specific and is documented on the corresponding [CoreWebView2DiagnosticCategory](corewebview2diagnosticcategory.md) value. Calling this method again for the same category replaces the previous filter. Returns `E_INVALIDARG` if the JSON is malformed or does not match the category's filter schema; on failure the filter state is unchanged.





## Events

### DiagnosticReceived

Raised when a diagnostic signal passes a filter set with [CoreWebView2DiagnosticMonitor.SetDiagnosticFilter](corewebview2diagnosticmonitor.md#setdiagnosticfilter).
The handler is invoked on the thread that created the environment. Multiple handlers can be registered and are invoked in registration order.


Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2DiagnosticMonitor, [CoreWebView2DiagnosticReceivedEventArgs](corewebview2diagnosticreceivedeventargs.md)&gt;



## Referenced by

- [CoreWebView2Environment](corewebview2environment.md)
