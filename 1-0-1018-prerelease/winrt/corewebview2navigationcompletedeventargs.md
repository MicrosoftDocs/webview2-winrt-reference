---
description: Event args for the CoreWebView2.NavigationCompleted event.
title: CoreWebView2NavigationCompletedEventArgs
ms.date: 09/21/2021
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2NavigationCompletedEventArgs
---

# CoreWebView2NavigationCompletedEventArgs Class



Event args for the [CoreWebView2.NavigationCompleted](corewebview2.md#navigationcompleted) event.

## Summary

Members|Description
--|--
[IsSuccess](#issuccess) | `true` when the navigation is successful; `false` for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx).
[NavigationId](#navigationid) | Gets the ID of the navigation.
[WebErrorStatus](#weberrorstatus) | Gets the error code if the navigation failed.

## Properties

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
