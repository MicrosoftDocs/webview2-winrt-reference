---
description: Specifies the process failure kind used in CoreWebView2ProcessFailedEventArgs. The values in this enum make reference to the process kinds in the Chromium architecture. For more information about what these processes are and what they do, see Browser Architecture - Inside look at modern web browser.
title: CoreWebView2ProcessFailedKind
ms.date: 11/06/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ProcessFailedKind
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- Microsoft.Web.WebView2.Core.CoreWebView2ProcessFailedKind
---

# CoreWebView2ProcessFailedKind Enum

Specifies the process failure kind used in [CoreWebView2ProcessFailedEventArgs](corewebview2processfailedeventargs.md). The values in this enum make reference to the process kinds in the Chromium architecture. For more information about what these processes are and what they do, see [Browser Architecture - Inside look at modern web browser](https://developers.google.com/web/updates/2018/09/inside-browser-part1).

| Name |  Value | Description |
|--|--|--|
|`BrowserProcessExited` | 0x0  |  Indicates that the browser process ended unexpectedly. The WebView automatically moves to the Closed state. The app has to recreate a new WebView to recover from this failure.|
|`RenderProcessExited` | 0x1  |  Indicates that the main frame's render process ended unexpectedly. Any subframes in the WebView will be gone too. A new render process is created automatically and navigated to an error page. You can use the [CoreWebView2.Reload](corewebview2.md#reload) method to try to recover from this failure. Alternatively, you can use [CoreWebView2Controller.Close](corewebview2controller.md#close) and recreate the WebView.|
|`RenderProcessUnresponsive` | 0x2  |  Indicates that the main frame's render process is unresponsive. Renderer process unresponsiveness can happen for the following reasons: There is a **long-running script** being executed. For example, the web content in your WebView might be performing a synchronous XHR, or have entered an infinite loop. Or, the **system is busy**. The `ProcessFailed` event will continue to be raised every few seconds until the renderer process has become responsive again. The application can consider taking action if the event keeps being raised. For example, the application might show UI for the user to decide to keep waiting or reload the page, or navigate away. |
|`FrameRenderProcessExited` | 0x3  |  Indicates that a frame-only render process ended unexpectedly. The process exit does not affect the top-level document, only a subset of the subframes within it. The content in these frames is replaced with an error page in the frame. Your application can communicate with the main frame to recover content in the impacted frames, using [CoreWebView2ProcessFailedEventArgs.FrameInfosForFailedProcess](corewebview2processfailedeventargs.md#frameinfosforfailedprocess) to get information about the impacted frames.|
|`UtilityProcessExited` | 0x4  |  Indicates that a utility process ended unexpectedly. The failed process is recreated automatically. Your application does not need to handle recovery for this event, but can use [CoreWebView2ProcessFailedEventArgs](corewebview2processfailedeventargs.md) to collect information about the failure, including `ProcessDescription`.|
|`SandboxHelperProcessExited` | 0x5  |  Indicates that a sandbox helper process ended unexpectedly. This failure is not fatal. Your application does not need to handle recovery for this event, but can use [CoreWebView2ProcessFailedEventArgs](corewebview2processfailedeventargs.md) to collect information about the failure.|
|`GpuProcessExited` | 0x6  |  Indicates that the GPU process ended unexpectedly. The failed process is recreated automatically. This failure is not fatal. Your application does not need to handle recovery for this event, but can use [CoreWebView2ProcessFailedEventArgs](corewebview2processfailedeventargs.md) to collect information about the failure.|
|`PpapiPluginProcessExited` | 0x7  |  Indicates that a PPAPI plugin process ended unexpectedly. This failure is not fatal. Your application does not need to handle recovery for this event, but can use [CoreWebView2ProcessFailedEventArgs](corewebview2processfailedeventargs.md) to collect information about the failure, including `ProcessDescription`.|
|`PpapiBrokerProcessExited` | 0x8  |  Indicates that a PPAPI plugin broker process ended unexpectedly. This failure is not fatal. Your application does not need to handle recovery for this event, but can use [CoreWebView2ProcessFailedEventArgs](corewebview2processfailedeventargs.md) to collect information about the failure.|
|`UnknownProcessExited` | 0x9  |  Indicates that a process of unspecified kind ended unexpectedly. Your application can use [CoreWebView2ProcessFailedEventArgs](corewebview2processfailedeventargs.md) to collect information about the failure.|


## Referenced by

- [CoreWebView2ProcessFailedEventArgs](corewebview2processfailedeventargs.md)
