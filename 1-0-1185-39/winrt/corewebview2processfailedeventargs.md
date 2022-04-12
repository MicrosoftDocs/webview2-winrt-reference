---
description: Event args for the CoreWebView2.ProcessFailed event.
title: CoreWebView2ProcessFailedEventArgs
ms.date: 04/07/2022
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ProcessFailedEventArgs
---

# CoreWebView2ProcessFailedEventArgs Class



Event args for the [CoreWebView2.ProcessFailed](corewebview2.md#processfailed) event.

## Summary

Members|Description
--|--
[ExitCode](#exitcode) | Gets the exit code of the failing process, for telemetry purposes.
[FrameInfosForFailedProcess](#frameinfosforfailedprocess) | Gets the collection of [CoreWebView2FrameInfo](corewebview2frameinfo.md)s for frames in the [CoreWebView2](corewebview2.md) that were being rendered by the failed process.
[ProcessDescription](#processdescription) | Gets a description of the failing process, assigned by the WebView2 Runtime.
[ProcessFailedKind](#processfailedkind) | Gets the kind of process failure that has occurred.
[Reason](#reason) | Gets the reason for the process failure.

## Properties

### ExitCode

> readonly  int ExitCode

Gets the exit code of the failing process, for telemetry purposes.
The exit code is always `STILL_ACTIVE`(`259`) when [CoreWebView2ProcessFailedEventArgs.ProcessFailedKind](corewebview2processfailedeventargs.md#processfailedkind) is [CoreWebView2ProcessFailedKind](corewebview2processfailedkind.md).RenderProcessUnresponsive.

### FrameInfosForFailedProcess

> readonly  [`IVectorView`](/uwp/api/Windows.Foundation.Collections.IVectorView-1)&lt;[CoreWebView2FrameInfo](corewebview2frameinfo.md)&gt; FrameInfosForFailedProcess

Gets the collection of [CoreWebView2FrameInfo](corewebview2frameinfo.md)s for frames in the [CoreWebView2](corewebview2.md) that were being rendered by the failed process.
This is only available when [CoreWebView2ProcessFailedEventArgs.ProcessFailedKind](corewebview2processfailedeventargs.md#processfailedkind) is [CoreWebView2ProcessFailedKind](corewebview2processfailedkind.md).FrameRenderProcessExited; the returned collection is empty for all other process failure kinds, including the case in which the failed process was the renderer for the main frame and subframes within it, for which the failure kind is [CoreWebView2ProcessFailedKind](corewebview2processfailedkind.md).RenderProcessExited.

### ProcessDescription

> readonly  string ProcessDescription

Gets a description of the failing process, assigned by the WebView2 Runtime.
This is a technical English term appropriate for logging or development purposes, and not localized for the end user. It applies to utility processes (for example, "Audio Service", "Video Capture") and plugin processes (for example, "Flash"). The returned string is empty if the WebView2 Runtime did not assign a description to the process.

### ProcessFailedKind

> readonly  [CoreWebView2ProcessFailedKind](corewebview2processfailedkind.md) ProcessFailedKind

Gets the kind of process failure that has occurred.
`ProcessFailedKind` is [CoreWebView2ProcessFailedKind](corewebview2processfailedkind.md).RenderProcessExited if the failed process is the main frame's renderer, even if there were subframes rendered by such process; all frames are gone when this happens.

### Reason

> readonly  [CoreWebView2ProcessFailedReason](corewebview2processfailedreason.md) Reason

Gets the reason for the process failure.
The reason is always [CoreWebView2ProcessFailedReason](corewebview2processfailedreason.md).Unexpected when [CoreWebView2ProcessFailedEventArgs.ProcessFailedKind](corewebview2processfailedeventargs.md#processfailedkind) is [CoreWebView2ProcessFailedKind](corewebview2processfailedkind.md).BrowserProcessExited, and [CoreWebView2ProcessFailedReason](corewebview2processfailedreason.md).Unresponsive when [CoreWebView2ProcessFailedEventArgs.ProcessFailedKind](corewebview2processfailedeventargs.md#processfailedkind) is [CoreWebView2ProcessFailedKind](corewebview2processfailedkind.md).RenderProcessUnresponsive. For other process failure kinds, the reason may be any of the reason values.






## Referenced by

- [CoreWebView2](corewebview2.md)
