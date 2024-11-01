---
title: CoreWebView2ProcessFailedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/01/2024
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ProcessFailedEventArgs
---

# runtimeClass CoreWebView2ProcessFailedEventArgs



## Summary

Members|Description
--|--
[ExitCode](#exitcode) | 
[FailureSourceModulePath](#failuresourcemodulepath) | 
[FrameInfosForFailedProcess](#frameinfosforfailedprocess) | 
[ProcessDescription](#processdescription) | 
[ProcessFailedKind](#processfailedkind) | 
[Reason](#reason) | 

## Properties

### ExitCode

> readonly  int ExitCode

### FailureSourceModulePath

> readonly  string FailureSourceModulePath

### FrameInfosForFailedProcess

> readonly  [`IVectorView`](/uwp/api/Windows.Foundation.Collections.IVectorView-1)&lt;[CoreWebView2FrameInfo](corewebview2frameinfo.md)&gt; FrameInfosForFailedProcess

### ProcessDescription

> readonly  string ProcessDescription

### ProcessFailedKind

> readonly  [CoreWebView2ProcessFailedKind](corewebview2processfailedkind.md) ProcessFailedKind

### Reason

> readonly  [CoreWebView2ProcessFailedReason](corewebview2processfailedreason.md) Reason






## Referenced by

- [CoreWebView2](corewebview2.md)
