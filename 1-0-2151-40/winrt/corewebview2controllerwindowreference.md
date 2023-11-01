---
description: 
title: CoreWebView2ControllerWindowReference
ms.date: 11/06/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ControllerWindowReference
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- Microsoft.Web.WebView2.Core.CoreWebView2ControllerWindowReference
- Microsoft.Web.WebView2.Core.CoreWebView2ControllerWindowReference.CoreWindow
- Microsoft.Web.WebView2.Core.CoreWebView2ControllerWindowReference.WindowHandle
- Microsoft.Web.WebView2.Core.CoreWebView2ControllerWindowReference.CreateFromCoreWindow
- Microsoft.Web.WebView2.Core.CoreWebView2ControllerWindowReference.CreateFromWindowHandle
- Microsoft.Web.WebView2.Core.CoreWebView2ControllerWindowReference.get_CoreWindow
- Microsoft.Web.WebView2.Core.CoreWebView2ControllerWindowReference.get_WindowHandle
---

# CoreWebView2ControllerWindowReference Class



## Summary

Members|Description
--|--
[CoreWindow](#corewindow) | 
[WindowHandle](#windowhandle) | 
[CreateFromCoreWindow](#createfromcorewindow) | 
[CreateFromWindowHandle](#createfromwindowhandle) | 

## Properties

### CoreWindow

> readonly  [CoreWindow](/uwp/api/Windows.UI.Core.CoreWindow) CoreWindow

### WindowHandle

> readonly  uint64_t WindowHandle



## Methods

### CreateFromCoreWindow

> static CoreWebView2ControllerWindowReference CreateFromCoreWindow([CoreWindow](/uwp/api/Windows.UI.Core.CoreWindow) coreWindow)



### CreateFromWindowHandle

> static CoreWebView2ControllerWindowReference CreateFromWindowHandle(uint64_t windowHandle)






## Referenced by

- [CoreWebView2Controller](corewebview2controller.md)
- [CoreWebView2Environment](corewebview2environment.md)
