---
title: CoreWebView2SaveFileSecurityCheckStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/13/2025
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2SaveFileSecurityCheckStartingEventArgs
---

# runtimeClass CoreWebView2SaveFileSecurityCheckStartingEventArgs



Event args for the [CoreWebView2.SaveFileSecurityCheckStarting](corewebview2.md#savefilesecuritycheckstarting) event.

## Summary

Members|Description
--|--
[CancelSave](#cancelsave) | Set if cancel the upcoming save/download.
[DocumentOriginUri](#documentoriginuri) | Get the document origin URI of this file save operation.
[FileExtension](#fileextension) | Get the extension of file to be saved.
[FilePath](#filepath) | Get the full path of file to be saved. This includes the file name and extension.
[SuppressDefaultPolicy](#suppressdefaultpolicy) | Set if the default policy checking and security warning will be suppressed.
[GetDeferral](#getdeferral) | Returns a Deferral object.

## Properties

### CancelSave

>  bool CancelSave

Set if cancel the upcoming save/download.

### DocumentOriginUri

> readonly  string DocumentOriginUri

Get the document origin URI of this file save operation.

### FileExtension

> readonly  string FileExtension

Get the extension of file to be saved.

### FilePath

> readonly  string FilePath

Get the full path of file to be saved. This includes the file name and extension.

### SuppressDefaultPolicy

>  bool SuppressDefaultPolicy

Set if the default policy checking and security warning will be suppressed.



## Methods

### GetDeferral

> [Deferral](/uwp/api/Windows.Foundation.Deferral) GetDeferral()

Returns a Deferral object.
It will put the event into a deferred state. The default policy checking and any default UI will be blocked temporarily, saving file to local won't start, until the deferral is completed.







## Referenced by

- [CoreWebView2](corewebview2.md)
