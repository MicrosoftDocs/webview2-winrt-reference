---
description: Specifies the process failure reason used in CoreWebView2ProcessFailedEventArgs.
title: CoreWebView2ProcessFailedReason
ms.date: 08/16/2021
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ProcessFailedReason
---

# CoreWebView2ProcessFailedReason Enum

Specifies the process failure reason used in [CoreWebView2ProcessFailedEventArgs](corewebview2processfailedeventargs.md).

| Name |  Value | Description |
|--|--|--|
|`Unexpected` | 0x0  |  Indicates that an unexpected process failure occurred.|
|`Unresponsive` | 0x1  |  Indicates that the process became unresponsive. This only applies to the main frame's render process.|
|`Terminated` | 0x2  |  Indicates that the process was terminated. For example, from Task Manager.|
|`Crashed` | 0x3  |  Indicates that the process crashed.|
|`LaunchFailed` | 0x4  |  Indicates that the process failed to launch.|
|`OutOfMemory` | 0x5  |  Indicates that the process died due to running out of memory.|


## Referenced by

- [CoreWebView2ProcessFailedEventArgs](corewebview2processfailedeventargs.md)