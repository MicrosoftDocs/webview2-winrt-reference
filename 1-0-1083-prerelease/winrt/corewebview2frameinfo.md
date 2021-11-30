---
description: Provides a set of properties for a frame in the CoreWebView2.
title: CoreWebView2FrameInfo
ms.date: 11/29/2021
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2FrameInfo
---

# CoreWebView2FrameInfo Class



Provides a set of properties for a frame in the [CoreWebView2](corewebview2.md).

## Summary

Members|Description
--|--
[Name](#name) | Gets the name attribute of the frame, as in `<iframe name="frame-name" ...>`.
[Source](#source) | The URI of the document in the frame.

## Properties

### Name

> readonly  string Name

Gets the name attribute of the frame, as in `<iframe name="frame-name" ...>`.
The returned string is empty when the frame has no name attribute.

### Source

> readonly  string Source

The URI of the document in the frame.




