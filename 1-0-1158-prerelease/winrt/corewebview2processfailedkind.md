---
description: Specifies the process failure kind used in CoreWebView2ProcessFailedEventArgs.
title: CoreWebView2ProcessFailedKind
ms.date: 02/10/2022
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ProcessFailedKind
---

# CoreWebView2ProcessFailedKind Enum

Specifies the process failure kind used in [CoreWebView2ProcessFailedEventArgs](corewebview2processfailedeventargs.md).
The values in this enum make reference to the process kinds in the Chromium architecture. For more information about what these processes are and what they do, see [Browser Architecture - Inside look at modern web browser](https://developers.google.com/web/updates/2018/09/inside-browser-part1).

| Name |  Value | Description |
|--|--|--|
|`BrowserProcessExited` | 0x0  |  Indicates that the browser process ended unexpectedly. The WebView automatically moves to the Closed state. The app has to recreate a new WebView to recover from this failure.|
|`RenderProcessExited` | 0x1  |  Indicates that the main frame's render process ended unexpectedly. A new render process is created automatically and navigated to an error page. You can use the [CoreWebView2.Reload](corewebview2.md#reload) method to try reload the page that failed.|
|`RenderProcessUnresponsive` | 0x2  |  Indicates that the main frame's render process is unresponsive.|
|`FrameRenderProcessExited` | 0x3  |  Indicates that a frame-only render process ended unexpectedly. The process exit does not affect the top-level document, only a subset of the subframes within it. The content in these frames is replaced with an error page in the frame.|
|`UtilityProcessExited` | 0x4  |  Indicates that a utility process ended unexpectedly.|
|`SandboxHelperProcessExited` | 0x5  |  Indicates that a sandbox helper process ended unexpectedly.|
|`GpuProcessExited` | 0x6  |  Indicates that the GPU process ended unexpectedly.|
|`PpapiPluginProcessExited` | 0x7  |  Indicates that a PPAPI plugin process ended unexpectedly.|
|`PpapiBrokerProcessExited` | 0x8  |  Indicates that a PPAPI plugin broker process ended unexpectedly.|
|`UnknownProcessExited` | 0x9  |  Indicates that a process of unspecified kind ended unexpectedly.|


## Referenced by

- [CoreWebView2ProcessFailedEventArgs](corewebview2processfailedeventargs.md)
