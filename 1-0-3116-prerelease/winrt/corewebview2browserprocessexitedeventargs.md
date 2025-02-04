---
description: Event args for the CoreWebView2Environment.BrowserProcessExited event.
title: CoreWebView2BrowserProcessExitedEventArgs
ms.date: 02/04/2025
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2BrowserProcessExitedEventArgs
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2BrowserProcessExitedEventArgs
- CoreWebView2BrowserProcessExitedEventArgs.BrowserProcessExitKind
- CoreWebView2BrowserProcessExitedEventArgs.BrowserProcessId
---

# CoreWebView2BrowserProcessExitedEventArgs Class



Event args for the [CoreWebView2Environment.BrowserProcessExited](corewebview2environment.md#browserprocessexited) event.

## Summary

Members|Description
--|--
[BrowserProcessExitKind](#browserprocessexitkind) | The kind of browser process exit that has occurred.
[BrowserProcessId](#browserprocessid) | The process ID of the browser process that has exited.

## Properties

### BrowserProcessExitKind

> readonly  [CoreWebView2BrowserProcessExitKind](corewebview2browserprocessexitkind.md) BrowserProcessExitKind

The kind of browser process exit that has occurred.

### BrowserProcessId

> readonly  uint32_t BrowserProcessId

The process ID of the browser process that has exited.






## Referenced by

- [CoreWebView2Environment](corewebview2environment.md)
