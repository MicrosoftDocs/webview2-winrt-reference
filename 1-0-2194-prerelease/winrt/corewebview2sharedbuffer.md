---
description: 
title: CoreWebView2SharedBuffer
ms.date: 11/06/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2SharedBuffer
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- Microsoft.Web.WebView2.Core.CoreWebView2SharedBuffer
- Microsoft.Web.WebView2.Core.CoreWebView2SharedBuffer.Buffer
- Microsoft.Web.WebView2.Core.CoreWebView2SharedBuffer.Size
- Microsoft.Web.WebView2.Core.CoreWebView2SharedBuffer.Close
- Microsoft.Web.WebView2.Core.CoreWebView2SharedBuffer.OpenStream
- Microsoft.Web.WebView2.Core.CoreWebView2SharedBuffer.get_Buffer
- Microsoft.Web.WebView2.Core.CoreWebView2SharedBuffer.get_Size
---

# CoreWebView2SharedBuffer Class

Implements: [IClosable](/uwp/api/Windows.Foundation.IClosable)

## Summary

Members|Description
--|--
[Buffer](#buffer) | 
[Size](#size) | 
[Close](#close) | 
[OpenStream](#openstream) | 

## Properties

### Buffer

> readonly  [IMemoryBufferReference](/uwp/api/Windows.Foundation.IMemoryBufferReference) Buffer

### Size

> readonly  uint64_t Size



## Methods

### Close

> void Close()



### OpenStream

> [IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) OpenStream()






## Referenced by

- [CoreWebView2](corewebview2.md)
- [CoreWebView2Environment](corewebview2environment.md)
- [CoreWebView2Frame](corewebview2frame.md)
