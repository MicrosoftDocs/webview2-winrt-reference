---
description: 
title: CoreWebView2DownloadOperation
ms.date: 10/16/2023
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



## Summary

Members|Description
--|--
[BytesReceived](#bytesreceived) | 
[CanResume](#canresume) | 
[ContentDisposition](#contentdisposition) | 
[EstimatedEndTime](#estimatedendtime) | 
[InterruptReason](#interruptreason) | 
[MimeType](#mimetype) | 
[ResultFilePath](#resultfilepath) | 
[State](#state) | 
[TotalBytesToReceive](#totalbytestoreceive) | 
[Uri](#uri) | 
[Cancel](#cancel) | 
[Pause](#pause) | 
[Resume](#resume) | 
[BytesReceivedChanged](#bytesreceivedchanged) | 
[EstimatedEndTimeChanged](#estimatedendtimechanged) | 
[StateChanged](#statechanged) | 

## Properties

### BytesReceived

> readonly  int64_t BytesReceived

### CanResume

> readonly  bool CanResume

### ContentDisposition

> readonly  string ContentDisposition

### EstimatedEndTime

> readonly  string EstimatedEndTime

### InterruptReason

> readonly  [CoreWebView2DownloadInterruptReason](corewebview2downloadinterruptreason.md) InterruptReason

### MimeType

> readonly  string MimeType

### ResultFilePath

> readonly  string ResultFilePath

### State

> readonly  [CoreWebView2DownloadState](corewebview2downloadstate.md) State

### TotalBytesToReceive

> readonly  int64_t TotalBytesToReceive

### Uri

> readonly  string Uri



## Methods

### Cancel

> void Cancel()



### Pause

> void Pause()



### Resume

> void Resume()




## Events

### BytesReceivedChanged

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2DownloadOperation, Object&gt;

### EstimatedEndTimeChanged

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2DownloadOperation, Object&gt;

### StateChanged

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2DownloadOperation, Object&gt;



## Referenced by

- [CoreWebView2DownloadStartingEventArgs](corewebview2downloadstartingeventargs.md)
