---
title: CoreWebView2ProcessFailedReason
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/13/2025
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ProcessFailedReason
---

# enum CoreWebView2ProcessFailedReason

Specifies the process failure reason used in [CoreWebView2ProcessFailedEventArgs](corewebview2processfailedeventargs.md). For process failures where a process has exited, it indicates the type of issue that produced the process exit.

| Name |  Value | Description |
|--|--|--|
|`Unexpected` | 0x0  |  Indicates that an unexpected process failure occurred.|
|`Unresponsive` | 0x1  |  Indicates that the process became unresponsive. This only applies to the main frame's render process.|
|`Terminated` | 0x2  |  Indicates that the process was terminated. For example, from Task Manager.|
|`Crashed` | 0x3  |  Indicates that the process crashed. Most crashes will generate dumps in the location indicated by [CoreWebView2Environment.FailureReportFolderPath](corewebview2environment.md#failurereportfolderpath).|
|`LaunchFailed` | 0x4  |  Indicates that the process failed to launch.|
|`OutOfMemory` | 0x5  |  Indicates that the process died due to running out of memory.|
|`ProfileDeleted` | 0x6  |  Deprecated. This value is unused.|


## Referenced by

- [CoreWebView2ProcessFailedEventArgs](corewebview2processfailedeventargs.md)
