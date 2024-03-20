---
description: Event args for the CoreWebView2.ProcessFailed event.
title: CoreWebView2ProcessFailedEventArgs
ms.date: 03/25/2024
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ProcessFailedEventArgs
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- Microsoft.Web.WebView2.Core.CoreWebView2ProcessFailedEventArgs
- Microsoft.Web.WebView2.Core.CoreWebView2ProcessFailedEventArgs.ExitCode
- Microsoft.Web.WebView2.Core.CoreWebView2ProcessFailedEventArgs.FailureSourceModulePath
- Microsoft.Web.WebView2.Core.CoreWebView2ProcessFailedEventArgs.FrameInfosForFailedProcess
- Microsoft.Web.WebView2.Core.CoreWebView2ProcessFailedEventArgs.ProcessDescription
- Microsoft.Web.WebView2.Core.CoreWebView2ProcessFailedEventArgs.ProcessFailedKind
- Microsoft.Web.WebView2.Core.CoreWebView2ProcessFailedEventArgs.Reason
- Microsoft.Web.WebView2.Core.CoreWebView2ProcessFailedEventArgs.get_ExitCode
- Microsoft.Web.WebView2.Core.CoreWebView2ProcessFailedEventArgs.get_FailureSourceModulePath
- Microsoft.Web.WebView2.Core.CoreWebView2ProcessFailedEventArgs.get_FrameInfosForFailedProcess
- Microsoft.Web.WebView2.Core.CoreWebView2ProcessFailedEventArgs.get_ProcessDescription
- Microsoft.Web.WebView2.Core.CoreWebView2ProcessFailedEventArgs.get_ProcessFailedKind
- Microsoft.Web.WebView2.Core.CoreWebView2ProcessFailedEventArgs.get_Reason
---

# CoreWebView2ProcessFailedEventArgs Class



Event args for the [CoreWebView2.ProcessFailed](corewebview2.md#processfailed) event.

## Summary

Members|Description
--|--
[ExitCode](#exitcode) | Gets the exit code of the failing process, for telemetry purposes.
[FailureSourceModulePath](#failuresourcemodulepath) | When ProcessFailed occurred due to a failed Code Integrity check, this property returns the full path of the file that was prevented from loading on the system.
[FrameInfosForFailedProcess](#frameinfosforfailedprocess) | Gets the collection of [CoreWebView2FrameInfo](corewebview2frameinfo.md)s for frames in the [CoreWebView2](corewebview2.md) that were being rendered by the failed process.
[ProcessDescription](#processdescription) | Gets a description of the failing process, assigned by the WebView2 Runtime.
[ProcessFailedKind](#processfailedkind) | Gets the kind of process failure that has occurred.
[Reason](#reason) | Gets the reason for the process failure.

## Properties

### ExitCode

> readonly  int ExitCode

Gets the exit code of the failing process, for telemetry purposes.
The exit code is always `STILL_ACTIVE`(`259`) when [CoreWebView2ProcessFailedEventArgs.ProcessFailedKind](corewebview2processfailedeventargs.md#processfailedkind) is [CoreWebView2ProcessFailedKind](corewebview2processfailedkind.md).RenderProcessUnresponsive.


### FailureSourceModulePath

> readonly  string FailureSourceModulePath

When ProcessFailed occurred due to a failed Code Integrity check, this property returns the full path of the file that was prevented from loading on the system.
The webview2 process which tried to load the DLL will fail with exit code STATUS_INVALID_IMAGE_HASH(-1073740760).

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
`ProcessFailedKind` is a combination of process kind (for example, browser, renderer, gpu) and failure (exit, unresponsiveness). Renderer processes are further divided in main frame renderer (`RenderProcessExited`, `RenderProcessUnresponsive`) and subframe renderer (`FrameRenderProcessExited`). To learn about the conditions under which each failure kind occurs, see [CoreWebView2ProcessFailedKind](corewebview2processfailedkind.md).


### Reason

> readonly  [CoreWebView2ProcessFailedReason](corewebview2processfailedreason.md) Reason

Gets the reason for the process failure.
Some of the reasons are only applicable to specific values of [CoreWebView2ProcessFailedEventArgs.ProcessFailedKind](corewebview2processfailedeventargs.md#processfailedkind), and the following [CoreWebView2ProcessFailedEventArgs.ProcessFailedKind](corewebview2processfailedeventargs.md#processfailedkind) values always return the indicated reason value:

ProcessFailedKind | Reason
---|---
`BrowserProcessExited` | `Unexpected`
`RenderProcessUnresponsive` | `Unresponsive`

For other [CoreWebView2ProcessFailedEventArgs.ProcessFailedKind](corewebview2processfailedeventargs.md#processfailedkind) values, the reason may be any of the reason values. To learn about what these values mean, see [CoreWebView2ProcessFailedReason](corewebview2processfailedreason.md).







## Referenced by

- [CoreWebView2](corewebview2.md)
