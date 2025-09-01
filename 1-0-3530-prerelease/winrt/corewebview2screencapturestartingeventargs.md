---
description: Event args for the CoreWebView2.ScreenCaptureStarting event.
title: CoreWebView2ScreenCaptureStartingEventArgs
ms.date: 09/01/2025
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ScreenCaptureStartingEventArgs
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2ScreenCaptureStartingEventArgs
- CoreWebView2ScreenCaptureStartingEventArgs.Cancel
- CoreWebView2ScreenCaptureStartingEventArgs.Handled
- CoreWebView2ScreenCaptureStartingEventArgs.OriginalSourceFrameInfo
- CoreWebView2ScreenCaptureStartingEventArgs.GetDeferral
---

# CoreWebView2ScreenCaptureStartingEventArgs Class



Event args for the [CoreWebView2.ScreenCaptureStarting](corewebview2.md#screencapturestarting) event.

## Summary

Members|Description
--|--
[Cancel](#cancel) | The host may set this flag to `TRUE` to cancel the screen capture.
[Handled](#handled) | The host may set this flag to `TRUE` to prevent the `ScreenCaptureStarting` event from firing on the `CoreWebView2` as well.
[OriginalSourceFrameInfo](#originalsourceframeinfo) | The frame info of the frame where the screen capture starting request originated.
[GetDeferral](#getdeferral) | Returns a Deferral object.

## Properties

### Cancel

>  bool Cancel

The host may set this flag to `TRUE` to cancel the screen capture.
If canceled, the screen capture UI is not displayed regardless of the `Handled` property. On the script side, it will return with a NotAllowedError as Permission denied.

### Handled

>  bool Handled

The host may set this flag to `TRUE` to prevent the `ScreenCaptureStarting` event from firing on the `CoreWebView2` as well.
By default, both the `ScreenCaptureStarting` event handlers on the `CoreWebView2Frame` and the `CoreWebView2` will be invoked, with the `CoreWebView2Frame` event handlers invoked first. The host may set this flag to `TRUE` within the `CoreWebView2Frame` event handlers to prevent the remaining `CoreWebView2` event handlers from being invoked. If the flag is set to `FALSE` within the `CoreWebView2Frame` event handlers, downstream handlers can update the `Cancel` property.

### OriginalSourceFrameInfo

> readonly  [CoreWebView2FrameInfo](corewebview2frameinfo.md) OriginalSourceFrameInfo

The frame info of the frame where the screen capture starting request originated.



## Methods

### GetDeferral

> [Deferral](/uwp/api/Windows.Foundation.Deferral) GetDeferral()

Returns a Deferral object.
Use this deferral to defer the decision to show the Screen Capture UI. getDisplayMedia() won't call its callbacks until the deferral is completed.






## Referenced by

- [CoreWebView2](corewebview2.md)
- [CoreWebView2Frame](corewebview2frame.md)
