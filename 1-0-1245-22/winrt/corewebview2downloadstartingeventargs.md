---
description: Event args for the CoreWebView2.DownloadStarting event.
title: CoreWebView2DownloadStartingEventArgs
ms.date: 06/14/2022
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2DownloadStartingEventArgs
---

# CoreWebView2DownloadStartingEventArgs Class



Event args for the [CoreWebView2.DownloadStarting](corewebview2.md#downloadstarting) event.

## Summary

Members|Description
--|--
[Cancel](#cancel) | Indicates whether to cancel the download.
[DownloadOperation](#downloadoperation) | Returns the [CoreWebView2DownloadOperation](corewebview2downloadoperation.md) for the download that has started.
[Handled](#handled) | Indicates whether to hide the default download dialog.
[ResultFilePath](#resultfilepath) | The path to the file.
[GetDeferral](#getdeferral) | Gets a Deferral object.

## Properties

### Cancel

>  bool Cancel

Indicates whether to cancel the download.
If canceled, the download save dialog is not displayed regardless of the [CoreWebView2DownloadStartingEventArgs.Handled](corewebview2downloadstartingeventargs.md#handled) value and the state is changed to [CoreWebView2DownloadState](corewebview2downloadstate.md).Interrupted with interrupt reason [CoreWebView2DownloadInterruptReason](corewebview2downloadinterruptreason.md).UserCanceled.

### DownloadOperation

> readonly  [CoreWebView2DownloadOperation](corewebview2downloadoperation.md) DownloadOperation

Returns the [CoreWebView2DownloadOperation](corewebview2downloadoperation.md) for the download that has started.

### Handled

>  bool Handled

Indicates whether to hide the default download dialog.
If set to true, the default download dialog is hidden for this download. The download progresses normally if it is not canceled, there will just be no default UI shown. By default the value is false and the default download dialog is shown.

### ResultFilePath

>  string ResultFilePath

The path to the file.
If setting the path, the host should ensure that it is an absolute path, including the file name, and that the path does not point to an existing file. If the path points to an existing file, the file will be overwritten. If the directory does not exist, it is created.



## Methods

### GetDeferral

> [Deferral](/uwp/api/Windows.Foundation.Deferral) GetDeferral()

Gets a Deferral object.
Use this to Complete the event at a later time.






## Referenced by

- [CoreWebView2](corewebview2.md)
