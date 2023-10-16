---
description: 
title: CoreWebView2WebResourceResponseView
ms.date: 10/16/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2WebResourceResponseView
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- Microsoft.Web.WebView2.Core.CoreWebView2WebResourceResponseView
- Microsoft.Web.WebView2.Core.CoreWebView2WebResourceResponseView.Headers
- Microsoft.Web.WebView2.Core.CoreWebView2WebResourceResponseView.ReasonPhrase
- Microsoft.Web.WebView2.Core.CoreWebView2WebResourceResponseView.StatusCode
- Microsoft.Web.WebView2.Core.CoreWebView2WebResourceResponseView.GetContentAsync
- Microsoft.Web.WebView2.Core.CoreWebView2WebResourceResponseView.get_Headers
- Microsoft.Web.WebView2.Core.CoreWebView2WebResourceResponseView.get_ReasonPhrase
- Microsoft.Web.WebView2.Core.CoreWebView2WebResourceResponseView.get_StatusCode
---

# CoreWebView2WebResourceResponseView Class



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
