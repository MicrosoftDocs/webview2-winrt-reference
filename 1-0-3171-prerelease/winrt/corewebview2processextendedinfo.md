---
description: Provides a set of properties for a process list with extended information in the CoreWebView2Environment.
title: CoreWebView2ProcessExtendedInfo
ms.date: 03/03/2025
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ProcessExtendedInfo
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2ProcessExtendedInfo
- CoreWebView2ProcessExtendedInfo.AssociatedFrameInfos
- CoreWebView2ProcessExtendedInfo.ProcessInfo
---

# CoreWebView2ProcessExtendedInfo Class



Provides a set of properties for a process list with extended information in the [CoreWebView2Environment](corewebview2environment.md).

## Summary

Members|Description
--|--
[AssociatedFrameInfos](#associatedframeinfos) | Provides the collection of associated CoreWebView2FrameInfos (unresolved reference) which are actively running (showing or hiding UI elements) in this renderer process.
[ProcessInfo](#processinfo) | Provides the [CoreWebView2ProcessInfo](corewebview2processinfo.md) of the current process.

## Properties

### AssociatedFrameInfos

> readonly  [`IVectorView`](/uwp/api/Windows.Foundation.Collections.IVectorView-1)&lt;[CoreWebView2FrameInfo](corewebview2frameinfo.md)&gt; AssociatedFrameInfos

Provides the collection of associated CoreWebView2FrameInfos (unresolved reference) which are actively running (showing or hiding UI elements) in this renderer process.
AssociatedFrameInfos will only be populated when this CoreWebView2ProcessExtendedInfo corresponds to a renderer process. Non-renderer processes will always have an empty AssociatedFrameInfo. AssociatedFrameInfos may also be empty for renderer processes that have no active frames.

### ProcessInfo

> readonly  [CoreWebView2ProcessInfo](corewebview2processinfo.md) ProcessInfo

Provides the [CoreWebView2ProcessInfo](corewebview2processinfo.md) of the current process.




