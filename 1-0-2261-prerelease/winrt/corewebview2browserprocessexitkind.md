---
description: Specifies the browser process exit kind used in CoreWebView2BrowserProcessExitedEventArgs.
title: CoreWebView2BrowserProcessExitKind
ms.date: 12/11/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2BrowserProcessExitKind
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- Microsoft.Web.WebView2.Core.CoreWebView2BrowserProcessExitKind
---

# CoreWebView2BrowserProcessExitKind Enum

Specifies the browser process exit kind used in [CoreWebView2BrowserProcessExitedEventArgs](corewebview2browserprocessexitedeventargs.md).

| Name |  Value | Description |
|--|--|--|
|`Normal` | 0x0  |  Indicates that the browser process ended normally.|
|`Failed` | 0x1  |  Indicates that the browser process ended unexpectedly. A [CoreWebView2.ProcessFailed](corewebview2.md#processfailed) event will also be raised to listening WebViews from the [CoreWebView2Environment](corewebview2environment.md) associated to the failed process.|


## Referenced by

- [CoreWebView2BrowserProcessExitedEventArgs](corewebview2browserprocessexitedeventargs.md)
