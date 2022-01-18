---
description: Event args for the CoreWebView2.NavigationStarting event.
title: CoreWebView2NavigationStartingEventArgs
ms.date: 01/18/2022
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2NavigationStartingEventArgs
---

# CoreWebView2NavigationStartingEventArgs Class



Event args for the [CoreWebView2.NavigationStarting](corewebview2.md#navigationstarting) event.

## Summary

Members|Description
--|--
[Cancel](#cancel) | Determines whether to cancel the navigation.
[IsRedirected](#isredirected) | `true` when the navigation is redirected.
[IsUserInitiated](#isuserinitiated) | `true` when the new window request was initiated through a user gesture.
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

`true` when the new window request was initiated through a user gesture.
Examples of user initiated requests are:
- Selecting an anchor tag with target
- Programmatic window open from a script that directly run as a result of user interaction such as via onclick handlers.
Non-user initiated requests are programmatic window opens from a script that are not directly triggered by user interaction, such as those that run while loading a new page or via timers.
The Microsoft Edge popup blocker is disabled for WebView so the app is able to use this flag to block non-user initiated popups.

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
