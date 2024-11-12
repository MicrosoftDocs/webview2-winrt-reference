---
title: CoreWebView2DownloadState
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/12/2024
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2DownloadState
---

# enum CoreWebView2DownloadState

The state of the [CoreWebView2DownloadOperation](corewebview2downloadoperation.md).

| Name |  Value | Description |
|--|--|--|
|`InProgress` | 0x0  |  The download is in progress.|
|`Interrupted` | 0x1  |  The connection with the file host was broken. The reason why a download was interrupted can accessed from [CoreWebView2DownloadOperation.InterruptReason](corewebview2downloadoperation.md#interruptreason). See [CoreWebView2DownloadInterruptReason](corewebview2downloadinterruptreason.md) for descriptions of the different kinds of interrupt reasons. Host can check whether an interrupted download can be resumed with [CoreWebView2DownloadOperation.CanResume](corewebview2downloadoperation.md#canresume). Once resumed, the download state is in progress.|
|`Completed` | 0x2  |  The download completed successfully.|


## Referenced by

- [CoreWebView2DownloadOperation](corewebview2downloadoperation.md)
