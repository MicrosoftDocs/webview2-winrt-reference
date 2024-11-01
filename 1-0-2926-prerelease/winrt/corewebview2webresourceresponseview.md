---
title: CoreWebView2WebResourceResponseView
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/01/2024
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2WebResourceResponseView
---

# runtimeClass CoreWebView2WebResourceResponseView



## Summary

Members|Description
--|--
[Headers](#headers) | 
[ReasonPhrase](#reasonphrase) | 
[StatusCode](#statuscode) | 
[GetContentAsync](#getcontentasync) | 

## Properties

### Headers

> readonly  [CoreWebView2HttpResponseHeaders](corewebview2httpresponseheaders.md) Headers

### ReasonPhrase

> readonly  string ReasonPhrase

### StatusCode

> readonly  int StatusCode



## Methods

### GetContentAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;[IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream)&gt; GetContentAsync()






## Referenced by

- [CoreWebView2WebResourceResponseReceivedEventArgs](corewebview2webresourceresponsereceivedeventargs.md)
