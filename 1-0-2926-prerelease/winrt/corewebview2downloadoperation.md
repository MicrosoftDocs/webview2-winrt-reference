---
title: CoreWebView2DownloadOperation
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/01/2024
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2DownloadOperation
---

# runtimeClass CoreWebView2DownloadOperation



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

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2DownloadOperation](corewebview2downloadoperation.md), Object&gt;

### EstimatedEndTimeChanged

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2DownloadOperation](corewebview2downloadoperation.md), Object&gt;

### StateChanged

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2DownloadOperation](corewebview2downloadoperation.md), Object&gt;



## Referenced by

- [CoreWebView2DownloadStartingEventArgs](corewebview2downloadstartingeventargs.md)
