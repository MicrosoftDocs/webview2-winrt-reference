---
description: A shared memory based buffer object that is created by CoreWebView2Environment.CreateSharedBuffer. The object is presented to script as ArrayBuffer when posted to script with CoreWebView2.PostSharedBufferToScript.
title: CoreWebView2SharedBuffer
ms.date: 05/27/2025
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2SharedBuffer
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2SharedBuffer
- CoreWebView2SharedBuffer.Buffer
- CoreWebView2SharedBuffer.Size
- CoreWebView2SharedBuffer.Close
- CoreWebView2SharedBuffer.OpenStream
---

# CoreWebView2SharedBuffer Class

Implements: [IClosable](/uwp/api/Windows.Foundation.IClosable)

A shared memory based buffer object that is created by [CoreWebView2Environment.CreateSharedBuffer](corewebview2environment.md#createsharedbuffer). The object is presented to script as ArrayBuffer when posted to script with [CoreWebView2.PostSharedBufferToScript](corewebview2.md#postsharedbuffertoscript).

## Summary

Members|Description
--|--
[Buffer](#buffer) | Returns an [IMemoryBufferReference](/uwp/api/Windows.Foundation.IMemoryBufferReference) object to access the underlying memory of the shared buffer as an array of bytes.
[Size](#size) | The size of the shared buffer in bytes.
[Close](#close) | 
[OpenStream](#openstream) | Get an stream object that can be used to access the shared buffer.

## Properties

### Buffer

> readonly  [IMemoryBufferReference](/uwp/api/Windows.Foundation.IMemoryBufferReference) Buffer

Returns an [IMemoryBufferReference](/uwp/api/Windows.Foundation.IMemoryBufferReference) object to access the underlying memory of the shared buffer as an array of bytes.

### Size

> readonly  uint64_t Size

The size of the shared buffer in bytes.



## Methods

### Close

> void Close()



### OpenStream

> [IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) OpenStream()

Get an stream object that can be used to access the shared buffer.






## Referenced by

- [CoreWebView2](corewebview2.md)
- [CoreWebView2Environment](corewebview2environment.md)
- [CoreWebView2Frame](corewebview2frame.md)
