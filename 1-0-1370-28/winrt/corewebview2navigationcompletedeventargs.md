---
description: Event args for the CoreWebView2.NavigationCompleted event.
title: CoreWebView2NavigationCompletedEventArgs
ms.date: 10/10/2022
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2NavigationCompletedEventArgs
---

# CoreWebView2NavigationCompletedEventArgs Class



Event args for the [CoreWebView2.NavigationCompleted](corewebview2.md#navigationcompleted) event.

## Summary

Members|Description
--|--
[HttpStatusCode](#httpstatuscode) | The HTTP status code of the navigation if it involved an HTTP request. For instance, this will usually be 200 if the request was successful, 404 if a page was not found, etc. See https://developer.mozilla.org/docs/Web/HTTP/Status for a list of common status codes.
[IsSuccess](#issuccess) | `true` when the navigation is successful; `false` for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx).
[NavigationId](#navigationid) | Gets the ID of the navigation.
[WebErrorStatus](#weberrorstatus) | Gets the error code if the navigation failed.

## Properties

### HttpStatusCode

> readonly  int HttpStatusCode

The HTTP status code of the navigation if it involved an HTTP request. For instance, this will usually be 200 if the request was successful, 404 if a page was not found, etc. See https://developer.mozilla.org/docs/Web/HTTP/Status for a list of common status codes.
The `HttpStatusCode` property will be 0 in the following cases:

- The navigation did not involve an HTTP request. For instance, if it was a navigation to a `file://` URL, or if it was a same-document navigation.
- The navigation failed before a response was received. For instance, if the hostname was not found, or if there was a network error.

In those cases, you can get more information from the [CoreWebView2NavigationCompletedEventArgs.IsSuccess](corewebview2navigationcompletedeventargs.md#issuccess) and [CoreWebView2NavigationCompletedEventArgs.WebErrorStatus](corewebview2navigationcompletedeventargs.md#weberrorstatus) properties.

If the navigation receives a successful HTTP response, but the navigated page calls `window.stop()` before it finishes loading, then HttpStatusCode may contain a success code like 200, but [CoreWebView2NavigationCompletedEventArgs.IsSuccess](corewebview2navigationcompletedeventargs.md#issuccess) will be `false` and [CoreWebView2NavigationCompletedEventArgs.WebErrorStatus](corewebview2navigationcompletedeventargs.md#weberrorstatus) will be [CoreWebView2WebErrorStatus](corewebview2weberrorstatus.md).ConnectionAborted.

Since WebView2 handles HTTP continuations and redirects automatically, it is unlikely for HttpStatusCode to ever be in the 1xx or 3xx ranges.

### IsSuccess

> readonly  bool IsSuccess

`true` when the navigation is successful; `false` for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx).
This may also be `false` for additional scenarios such as `window.stop()` run on navigated page.

### NavigationId

> readonly  uint64_t NavigationId

Gets the ID of the navigation.

### WebErrorStatus

> readonly  [CoreWebView2WebErrorStatus](corewebview2weberrorstatus.md) WebErrorStatus

Gets the error code if the navigation failed.






## Referenced by

- [CoreWebView2](corewebview2.md)
- [CoreWebView2Frame](corewebview2frame.md)
