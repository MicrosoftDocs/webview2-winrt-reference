---
title: CoreWebView2ProcessExtendedInfo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/12/2024
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ProcessExtendedInfo
---

# runtimeClass CoreWebView2ProcessExtendedInfo



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
AssociatedFrameInfos will only be populated when this [CoreWebView2ProcessExtendedInfo](corewebview2processextendedinfo.md) corresponds to a renderer process. Non-renderer processes will always have an empty AssociatedFrameInfo. AssociatedFrameInfos may also be empty for renderer processes that have no active frames.

### ProcessInfo

> readonly  [CoreWebView2ProcessInfo](corewebview2processinfo.md) ProcessInfo

Provides the [CoreWebView2ProcessInfo](corewebview2processinfo.md) of the current process.




