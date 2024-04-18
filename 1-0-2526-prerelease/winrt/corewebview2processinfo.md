---
description: Provides a set of properties for a process list in the CoreWebView2Environment.
title: CoreWebView2ProcessInfo
ms.date: 04/22/2024
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ProcessInfo
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- Microsoft.Web.WebView2.Core.CoreWebView2ProcessInfo
- Microsoft.Web.WebView2.Core.CoreWebView2ProcessInfo.AssociatedFrameInfos
- Microsoft.Web.WebView2.Core.CoreWebView2ProcessInfo.Kind
- Microsoft.Web.WebView2.Core.CoreWebView2ProcessInfo.ProcessId
- Microsoft.Web.WebView2.Core.CoreWebView2ProcessInfo.get_AssociatedFrameInfos
- Microsoft.Web.WebView2.Core.CoreWebView2ProcessInfo.get_Kind
- Microsoft.Web.WebView2.Core.CoreWebView2ProcessInfo.get_ProcessId
---

# CoreWebView2ProcessInfo Class



Provides a set of properties for a process list in the [CoreWebView2Environment](corewebview2environment.md).

## Summary

Members|Description
--|--
[AssociatedFrameInfos](#associatedframeinfos) | Provides the collection of associated CoreWebView2FrameInfos (unresolved reference) which are actively running (showing UI elements) in this renderer process.
[Kind](#kind) | Get the kind of the process.
[ProcessId](#processid) | Get the process id of the process.

## Properties

### AssociatedFrameInfos

> readonly  [`IVectorView`](/uwp/api/Windows.Foundation.Collections.IVectorView-1)&lt;[CoreWebView2FrameInfo](corewebview2frameinfo.md)&gt; AssociatedFrameInfos

Provides the collection of associated CoreWebView2FrameInfos (unresolved reference) which are actively running (showing UI elements) in this renderer process.
AssociatedFrameInfos will only be populated when obtained via calling [CoreWebView2Environment.GetProcessInfosWithDetailsAsync](corewebview2environment.md#getprocessinfoswithdetailsasync) and when this CoreWebView2ProcessInfo corresponds to a renderer process. CoreWebView2ProcessInfo objects obtained via [CoreWebView2Environment.GetProcessInfos](corewebview2environment.md#getprocessinfos) or for non-renderer processes will always have an empty AssociatedFrameInfo. AssociatedFrameInfos may also be empty for renderer processes that have no active frames.

### Kind

> readonly  [CoreWebView2ProcessKind](corewebview2processkind.md) Kind

Get the kind of the process.

### ProcessId

> readonly  int ProcessId

Get the process id of the process.






## Referenced by

- [CoreWebView2ProcessExtendedInfo](corewebview2processextendedinfo.md)
