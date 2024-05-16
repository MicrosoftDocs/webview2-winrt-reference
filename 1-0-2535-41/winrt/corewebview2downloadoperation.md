---
description: Represents a download operation. Gives access to a download's metadata and supports a user canceling, pausing, or resuming a download.
title: CoreWebView2DownloadOperation
ms.date: 05/20/2024
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2DownloadOperation
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- Microsoft.Web.WebView2.Core.CoreWebView2DownloadOperation
- Microsoft.Web.WebView2.Core.CoreWebView2DownloadOperation.BytesReceived
- Microsoft.Web.WebView2.Core.CoreWebView2DownloadOperation.CanResume
- Microsoft.Web.WebView2.Core.CoreWebView2DownloadOperation.ContentDisposition
- Microsoft.Web.WebView2.Core.CoreWebView2DownloadOperation.EstimatedEndTime
- Microsoft.Web.WebView2.Core.CoreWebView2DownloadOperation.InterruptReason
- Microsoft.Web.WebView2.Core.CoreWebView2DownloadOperation.MimeType
- Microsoft.Web.WebView2.Core.CoreWebView2DownloadOperation.ResultFilePath
- Microsoft.Web.WebView2.Core.CoreWebView2DownloadOperation.State
- Microsoft.Web.WebView2.Core.CoreWebView2DownloadOperation.TotalBytesToReceive
- Microsoft.Web.WebView2.Core.CoreWebView2DownloadOperation.Uri
- Microsoft.Web.WebView2.Core.CoreWebView2DownloadOperation.Cancel
- Microsoft.Web.WebView2.Core.CoreWebView2DownloadOperation.Pause
- Microsoft.Web.WebView2.Core.CoreWebView2DownloadOperation.Resume
- Microsoft.Web.WebView2.Core.CoreWebView2DownloadOperation.add_BytesReceivedChanged
- Microsoft.Web.WebView2.Core.CoreWebView2DownloadOperation.add_EstimatedEndTimeChanged
- Microsoft.Web.WebView2.Core.CoreWebView2DownloadOperation.add_StateChanged
- Microsoft.Web.WebView2.Core.CoreWebView2DownloadOperation.get_BytesReceived
- Microsoft.Web.WebView2.Core.CoreWebView2DownloadOperation.get_CanResume
- Microsoft.Web.WebView2.Core.CoreWebView2DownloadOperation.get_ContentDisposition
- Microsoft.Web.WebView2.Core.CoreWebView2DownloadOperation.get_EstimatedEndTime
- Microsoft.Web.WebView2.Core.CoreWebView2DownloadOperation.get_InterruptReason
- Microsoft.Web.WebView2.Core.CoreWebView2DownloadOperation.get_MimeType
- Microsoft.Web.WebView2.Core.CoreWebView2DownloadOperation.get_ResultFilePath
- Microsoft.Web.WebView2.Core.CoreWebView2DownloadOperation.get_State
- Microsoft.Web.WebView2.Core.CoreWebView2DownloadOperation.get_TotalBytesToReceive
- Microsoft.Web.WebView2.Core.CoreWebView2DownloadOperation.get_Uri
- Microsoft.Web.WebView2.Core.CoreWebView2DownloadOperation.remove_BytesReceivedChanged
- Microsoft.Web.WebView2.Core.CoreWebView2DownloadOperation.remove_EstimatedEndTimeChanged
- Microsoft.Web.WebView2.Core.CoreWebView2DownloadOperation.remove_StateChanged
- Microsoft.Web.WebView2.Core.CoreWebView2DownloadOperation.BytesReceivedChanged
- Microsoft.Web.WebView2.Core.CoreWebView2DownloadOperation.EstimatedEndTimeChanged
- Microsoft.Web.WebView2.Core.CoreWebView2DownloadOperation.StateChanged
---

# CoreWebView2DownloadOperation Class



Represents a download operation. Gives access to a download's metadata and supports a user canceling, pausing, or resuming a download.

## Summary

Members|Description
--|--
[BytesReceived](#bytesreceived) | The number of bytes that have been written to the download file.
[CanResume](#canresume) | Returns true if an interrupted download can be resumed.
[ContentDisposition](#contentdisposition) | The Content-Disposition header value from the download's HTTP response. If none, the value is an empty string.
[EstimatedEndTime](#estimatedendtime) | The estimated end time of the download.
[InterruptReason](#interruptreason) | The reason why connection with file host was broken.
[MimeType](#mimetype) | MIME type of the downloaded content.
[ResultFilePath](#resultfilepath) | The absolute path to the download file, including file name.
[State](#state) | The state of the download. A download can be in progress, interrupted, or completed.
[TotalBytesToReceive](#totalbytestoreceive) | The expected size of the download in total number of bytes based on the HTTP Content-Length header.
[Uri](#uri) | The URI of the download.
[Cancel](#cancel) | Cancels the download.
[Pause](#pause) | Pauses the download.
[Resume](#resume) | Resumes a paused download. May also resume a download that was interrupted for another reason if [CoreWebView2DownloadOperation.CanResume](corewebview2downloadoperation.md#canresume) returns true.
[BytesReceivedChanged](#bytesreceivedchanged) | Event raised when the bytes received count is updated.
[EstimatedEndTimeChanged](#estimatedendtimechanged) | Event raised when the estimated end time changes.
[StateChanged](#statechanged) | Event raised when the state of the download changes.

## Properties

### BytesReceived

> readonly  int64_t BytesReceived

The number of bytes that have been written to the download file.

### CanResume

> readonly  bool CanResume

Returns true if an interrupted download can be resumed.
Downloads with the following interrupt reasons may automatically resume without you calling any methods: [CoreWebView2DownloadInterruptReason](corewebview2downloadinterruptreason.md).ServerNoRange, [CoreWebView2DownloadInterruptReason](corewebview2downloadinterruptreason.md).FileHashMismatch, [CoreWebView2DownloadInterruptReason](corewebview2downloadinterruptreason.md).FileTooShort. In these cases progress may be restarted with [CoreWebView2DownloadOperation.BytesReceived](corewebview2downloadoperation.md#bytesreceived) set to 0.

### ContentDisposition

> readonly  string ContentDisposition

The Content-Disposition header value from the download's HTTP response. If none, the value is an empty string.

### EstimatedEndTime

> readonly  string EstimatedEndTime

The estimated end time of the download.

### InterruptReason

> readonly  [CoreWebView2DownloadInterruptReason](corewebview2downloadinterruptreason.md) InterruptReason

The reason why connection with file host was broken.
See [CoreWebView2DownloadInterruptReason](corewebview2downloadinterruptreason.md) for descriptions of reasons.

### MimeType

> readonly  string MimeType

MIME type of the downloaded content.

### ResultFilePath

> readonly  string ResultFilePath

The absolute path to the download file, including file name.
Host can change this from [CoreWebView2DownloadStartingEventArgs.ResultFilePath](corewebview2downloadstartingeventargs.md#resultfilepath).

### State

> readonly  [CoreWebView2DownloadState](corewebview2downloadstate.md) State

The state of the download. A download can be in progress, interrupted, or completed.
See [CoreWebView2DownloadState](corewebview2downloadstate.md) for descriptions of states.

### TotalBytesToReceive

> readonly  int64_t TotalBytesToReceive

The expected size of the download in total number of bytes based on the HTTP Content-Length header.
Returns null if the size is unknown.

### Uri

> readonly  string Uri

The URI of the download.



## Methods

### Cancel

> void Cancel()

Cancels the download.
If canceled, the default download dialog shows that the download was canceled. Host should use [CoreWebView2DownloadStartingEventArgs.Cancel](corewebview2downloadstartingeventargs.md#cancel) if download should be canceled without displaying the default download dialog.



### Pause

> void Pause()

Pauses the download.
If paused, the default download dialog shows that the download is paused. No effect if download is already paused. Pausing a download changes the state from in progress to interrupted, with interrupt reason set to [CoreWebView2DownloadInterruptReason](corewebview2downloadinterruptreason.md).UserCanceled.



### Resume

> void Resume()

Resumes a paused download. May also resume a download that was interrupted for another reason if [CoreWebView2DownloadOperation.CanResume](corewebview2downloadoperation.md#canresume) returns true.
Resuming a download changes the state from interrupted to in progress.




## Events

### BytesReceivedChanged

Event raised when the bytes received count is updated.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2DownloadOperation, Object&gt;

### EstimatedEndTimeChanged

Event raised when the estimated end time changes.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2DownloadOperation, Object&gt;

### StateChanged

Event raised when the state of the download changes.
Use CoreWebView2DownloadOperation.State to get the current state, and CoreWebView2DownloadOperation.InterruptReason to get the reason if the download is interrupted.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2DownloadOperation, Object&gt;



## Referenced by

- [CoreWebView2DownloadStartingEventArgs](corewebview2downloadstartingeventargs.md)
