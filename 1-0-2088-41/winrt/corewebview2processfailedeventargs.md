---
description: 
title: CoreWebView2ProcessFailedEventArgs
ms.date: 10/16/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ProcessFailedEventArgs
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- Microsoft.Web.WebView2.Core.CoreWebView2ProcessFailedEventArgs
- Microsoft.Web.WebView2.Core.CoreWebView2ProcessFailedEventArgs.ExitCode
- Microsoft.Web.WebView2.Core.CoreWebView2ProcessFailedEventArgs.FrameInfosForFailedProcess
- Microsoft.Web.WebView2.Core.CoreWebView2ProcessFailedEventArgs.ProcessDescription
- Microsoft.Web.WebView2.Core.CoreWebView2ProcessFailedEventArgs.ProcessFailedKind
- Microsoft.Web.WebView2.Core.CoreWebView2ProcessFailedEventArgs.Reason
- Microsoft.Web.WebView2.Core.CoreWebView2ProcessFailedEventArgs.get_ExitCode
- Microsoft.Web.WebView2.Core.CoreWebView2ProcessFailedEventArgs.get_FrameInfosForFailedProcess
- Microsoft.Web.WebView2.Core.CoreWebView2ProcessFailedEventArgs.get_ProcessDescription
- Microsoft.Web.WebView2.Core.CoreWebView2ProcessFailedEventArgs.get_ProcessFailedKind
- Microsoft.Web.WebView2.Core.CoreWebView2ProcessFailedEventArgs.get_Reason
---

# CoreWebView2ProcessFailedEventArgs Class



## Summary

Members|Description
--|--
[ExitCode](#exitcode) | 
[FrameInfosForFailedProcess](#frameinfosforfailedprocess) | 
[ProcessDescription](#processdescription) | 
[ProcessFailedKind](#processfailedkind) | 
[Reason](#reason) | 

## Properties

### ExitCode

> readonly  int ExitCode

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
