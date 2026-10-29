---
description: Event args for the CoreWebView2.ScreenCaptureStarting and CoreWebView2Frame.ScreenCaptureStarting events.
title: CoreWebView2ScreenCaptureStartingEventArgs
ms.date: 10/29/2026
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



Event args for the [CoreWebView2.ScreenCaptureStarting](corewebview2.md#screencapturestarting) and [CoreWebView2Frame.ScreenCaptureStarting](corewebview2frame.md#screencapturestarting) events.

## Summary

Members|Description
--|--
[Cancel](#cancel) | The host may set this flag to cancel the screen capture.
[Handled](#handled) | By default, both the [CoreWebView2Frame.ScreenCaptureStarting](corewebview2frame.md#screencapturestarting) event handlers on the [CoreWebView2Frame](corewebview2frame.md) and the [CoreWebView2.ScreenCaptureStarting](corewebview2.md#screencapturestarting) event handlers on the [CoreWebView2](corewebview2.md) will be invoked, with the [CoreWebView2Frame](corewebview2frame.md) event handlers invoked first.
[OriginalSourceFrameInfo](#originalsourceframeinfo) | The associated frame information that requests the screen capture permission.
[GetDeferral](#getdeferral) | Gets a Deferral object.

## Properties

### Cancel

>  bool Cancel

The host may set this flag to cancel the screen capture.
If canceled, the screen capture UI is not displayed regardless of the [CoreWebView2ScreenCaptureStartingEventArgs.Handled](corewebview2screencapturestartingeventargs.md#handled) property.
On the script side, it will return with a NotAllowedError as Permission denied.

### Handled

>  bool Handled

By default, both the [CoreWebView2Frame.ScreenCaptureStarting](corewebview2frame.md#screencapturestarting) event handlers on the [CoreWebView2Frame](corewebview2frame.md) and the [CoreWebView2.ScreenCaptureStarting](corewebview2.md#screencapturestarting) event handlers on the [CoreWebView2](corewebview2.md) will be invoked, with the [CoreWebView2Frame](corewebview2frame.md) event handlers invoked first.
The host may set this flag to `true` within the [CoreWebView2Frame](corewebview2frame.md) event handlers to prevent the remaining [CoreWebView2](corewebview2.md) event handlers from being invoked. If the flag is set to `false` within the [CoreWebView2Frame](corewebview2frame.md) event handlers, downstream handlers can update the [CoreWebView2ScreenCaptureStartingEventArgs.Cancel](corewebview2screencapturestartingeventargs.md#cancel) property.

If a deferral is taken on the event args, then you must synchronously set [CoreWebView2ScreenCaptureStartingEventArgs.Handled](corewebview2screencapturestartingeventargs.md#handled) to `true` prior to taking your deferral to prevent the [CoreWebView2](corewebview2.md) event handlers from being invoked.

### OriginalSourceFrameInfo

> readonly  [CoreWebView2FrameInfo](corewebview2frameinfo.md) OriginalSourceFrameInfo

The associated frame information that requests the screen capture permission.
This can be used to get the frame source, name, frameId, and parent frame information.



## Methods

### GetDeferral

> [Deferral](/uwp/api/Windows.Foundation.Deferral) GetDeferral()

Gets a Deferral object.
Use this deferral to defer the decision to show the Screen Capture UI. getDisplayMedia() won't call its callbacks until the deferral is completed.






## Referenced by

- [CoreWebView2](corewebview2.md)
- [CoreWebView2Frame](corewebview2frame.md)
