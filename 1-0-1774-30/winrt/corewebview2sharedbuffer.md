---
title: CoreWebView2SharedBuffer
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2023
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2SharedBuffer
---

# runtimeClass CoreWebView2SharedBuffer

Implements: [IClosable](/uwp/api/Windows.Foundation.IClosable)

A shared memory based buffer object that is created by [CoreWebView2Environment.CreateSharedBuffer](corewebview2environment.md#createsharedbuffer).

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
