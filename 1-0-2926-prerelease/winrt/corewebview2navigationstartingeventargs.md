---
title: CoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/01/2024
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2NavigationStartingEventArgs
---

# runtimeClass CoreWebView2NavigationStartingEventArgs



## Summary

Members|Description
--|--
[AdditionalAllowedFrameAncestors](#additionalallowedframeancestors) | 
[Cancel](#cancel) | 
[IsRedirected](#isredirected) | 
[IsUserInitiated](#isuserinitiated) | 
[NavigationId](#navigationid) | 
[NavigationKind](#navigationkind) | 
[RequestHeaders](#requestheaders) | 
[Uri](#uri) | 

## Properties

### AdditionalAllowedFrameAncestors

>  string AdditionalAllowedFrameAncestors

### Cancel

>  bool Cancel

### IsRedirected

> readonly  bool IsRedirected

### IsUserInitiated

> readonly  bool IsUserInitiated

### NavigationId

> readonly  uint64_t NavigationId

### NavigationKind

> readonly  [CoreWebView2NavigationKind](corewebview2navigationkind.md) NavigationKind

### RequestHeaders

> readonly  [CoreWebView2HttpRequestHeaders](corewebview2httprequestheaders.md) RequestHeaders

### Uri

> readonly  string Uri






## Referenced by

- [CoreWebView2](corewebview2.md)
- [CoreWebView2Frame](corewebview2frame.md)
