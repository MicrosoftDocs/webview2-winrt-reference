---
title: CoreWebView2ContentLoadingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/12/2021
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ContentLoadingEventArgs
---

# runtimeClass CoreWebView2ContentLoadingEventArgs



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
