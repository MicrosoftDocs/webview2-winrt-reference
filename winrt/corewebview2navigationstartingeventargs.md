---
title: CoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/12/2021
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2NavigationStartingEventArgs
---

# runtimeClass CoreWebView2NavigationStartingEventArgs



Event args for the [CoreWebView2.NavigationStarting](corewebview2.md#navigationstarting) event.

## Summary

Members|Description
--|--
[Cancel](#cancel) | Determines whether to cancel the navigation.
[IsRedirected](#isredirected) | `true` when the navigation is redirected.
[IsUserInitiated](#isuserinitiated) | `true` when the navigation was initiated through a user gesture as opposed to programmatic navigation.
[NavigationId](#navigationid) | Gets the ID of the navigation.
[RequestHeaders](#requestheaders) | Gets the HTTP request headers for the navigation.
[Uri](#uri) | Gets the uri of the requested navigation.

## Properties

### Cancel

>  bool Cancel

Determines whether to cancel the navigation.

If set to `true`, the navigation is no longer present and the content of the current page is intact. For performance reasons, `GET` HTTP requests may happen, while the host is responding. You may set cookies and use part of a request for the navigation. Cancellation for navigation to `about:blank` or frame navigation to srcdoc is not supported and ignored.

### IsRedirected

> readonly  bool IsRedirected

`true` when the navigation is redirected.

### IsUserInitiated

> readonly  bool IsUserInitiated

`true` when the navigation was initiated through a user gesture as opposed to programmatic navigation.

### NavigationId

> readonly  uint64_t NavigationId

Gets the ID of the navigation.

### RequestHeaders

> readonly  [CoreWebView2HttpRequestHeaders](corewebview2httprequestheaders.md) RequestHeaders

Gets the HTTP request headers for the navigation.

Note, you are not able to modify the HTTP request headers in a [CoreWebView2.NavigationStarting](corewebview2.md#navigationstarting) event.

### Uri

> readonly  string Uri

Gets the uri of the requested navigation.






## Referenced by

- [CoreWebView2](corewebview2.md)
- [CoreWebView2Frame](corewebview2frame.md)
