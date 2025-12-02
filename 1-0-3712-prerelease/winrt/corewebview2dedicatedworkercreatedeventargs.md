---
description: Event args for CoreWebView2.DedicatedWorkerCreated, CoreWebView2Frame.DedicatedWorkerCreated, and CoreWebView2DedicatedWorker.DedicatedWorkerCreated events.
title: CoreWebView2DedicatedWorkerCreatedEventArgs
ms.date: 12/02/2025
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2DedicatedWorkerCreatedEventArgs
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2DedicatedWorkerCreatedEventArgs
- CoreWebView2DedicatedWorkerCreatedEventArgs.OriginalSourceFrameInfo
- CoreWebView2DedicatedWorkerCreatedEventArgs.Worker
---

# CoreWebView2DedicatedWorkerCreatedEventArgs Class



Event args for [CoreWebView2.DedicatedWorkerCreated](corewebview2.md#dedicatedworkercreated), [CoreWebView2Frame.DedicatedWorkerCreated](corewebview2frame.md#dedicatedworkercreated), and [CoreWebView2DedicatedWorker.DedicatedWorkerCreated](corewebview2dedicatedworker.md#dedicatedworkercreated) events.


## Summary

Members|Description
--|--
[OriginalSourceFrameInfo](#originalsourceframeinfo) | The associated frame information that created the dedicated worker. This can be used to get the frame source, name, frameId, and parent frame information.
[Worker](#worker) | The dedicated worker that was created.

## Properties

### OriginalSourceFrameInfo

> readonly  [CoreWebView2FrameInfo](corewebview2frameinfo.md) OriginalSourceFrameInfo

The associated frame information that created the dedicated worker. This can be used to get the frame source, name, frameId, and parent frame information.


### Worker

> readonly  [CoreWebView2DedicatedWorker](corewebview2dedicatedworker.md) Worker

The dedicated worker that was created.







## Referenced by

- [CoreWebView2](corewebview2.md)
- [CoreWebView2DedicatedWorker](corewebview2dedicatedworker.md)
- [CoreWebView2Frame](corewebview2frame.md)
