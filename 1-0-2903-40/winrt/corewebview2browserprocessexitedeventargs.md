---
title: CoreWebView2BrowserProcessExitedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/12/2024
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2BrowserProcessExitedEventArgs
---

# runtimeClass CoreWebView2BrowserProcessExitedEventArgs



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
