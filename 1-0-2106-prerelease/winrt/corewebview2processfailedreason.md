---
description: Specifies the process failure reason used in CoreWebView2ProcessFailedEventArgs. For process failures where a process has exited, it indicates the type of issue that produced the process exit.
title: CoreWebView2ProcessFailedReason
ms.date: 9/19/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ProcessFailedReason
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- Microsoft.Web.WebView2.Core.CoreWebView2ProcessFailedReason
---

# CoreWebView2ProcessFailedReason Enum

Specifies the process failure reason used in [CoreWebView2ProcessFailedEventArgs](corewebview2processfailedeventargs.md). For process failures where a process has exited, it indicates the type of issue that produced the process exit.

| Name |  Value | Description |
|--|--|--|
|`Unexpected` | 0x0  |  Indicates that an unexpected process failure occurred.|
|`Unresponsive` | 0x1  |  Indicates that the process became unresponsive. This only applies to the main frame's render process.|
|`Terminated` | 0x2  |  Indicates that the process was terminated. For example, from Task Manager.|
|`Crashed` | 0x3  |  Indicates that the process crashed. Most crashes will generate dumps in the location indicated by [CoreWebView2Environment.FailureReportFolderPath](corewebview2environment.md#failurereportfolderpath).|
|`LaunchFailed` | 0x4  |  Indicates that the process failed to launch.|
|`OutOfMemory` | 0x5  |  Indicates that the process died due to running out of memory.|
|`ProfileDeleted` | 0x6  |  Indicates the webview2's profile has been deleted.|


## Referenced by

- [CoreWebView2ProcessFailedEventArgs](corewebview2processfailedeventargs.md)
