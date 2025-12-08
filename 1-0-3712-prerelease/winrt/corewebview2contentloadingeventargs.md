---
description: Event args for the CoreWebView2.ContentLoading event.
title: CoreWebView2ContentLoadingEventArgs
ms.date: 12/02/2025
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ContentLoadingEventArgs
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2ContentLoadingEventArgs
- CoreWebView2ContentLoadingEventArgs.IsErrorPage
- CoreWebView2ContentLoadingEventArgs.NavigationId
---

# CoreWebView2ContentLoadingEventArgs Class



Event args for the [CoreWebView2.ContentLoading](corewebview2.md#contentloading) event.

## Summary

Members|Description
--|--
[IsErrorPage](#iserrorpage) | `true` if the loaded content is an error page.
[NavigationId](#navigationid) | Gets the ID of the navigation.

## Properties

### IsErrorPage

> readonly  bool IsErrorPage

`true` if the loaded content is an error page.

### NavigationId

> readonly  uint64_t NavigationId

Gets the ID of the navigation.






## Referenced by

- [CoreWebView2](corewebview2.md)
- [CoreWebView2Frame](corewebview2frame.md)
