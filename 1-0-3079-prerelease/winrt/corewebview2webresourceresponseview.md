---
description: View of the HTTP representation for a web resource response.
title: CoreWebView2WebResourceResponseView
ms.date: 01/16/2025
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2WebResourceResponseView
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2WebResourceResponseView
- CoreWebView2WebResourceResponseView.Headers
- CoreWebView2WebResourceResponseView.ReasonPhrase
- CoreWebView2WebResourceResponseView.StatusCode
- CoreWebView2WebResourceResponseView.GetContentAsync
---

# CoreWebView2WebResourceResponseView Class



View of the HTTP representation for a web resource response.
The properties of this object are not mutable. This response view is used with the [CoreWebView2.WebResourceResponseReceived](corewebview2.md#webresourceresponsereceived) event.

## Summary

Members|Description
--|--
[Headers](#headers) | Gets the HTTP response headers as received.
[ReasonPhrase](#reasonphrase) | Gets the HTTP response reason phrase.
[StatusCode](#statuscode) | Gets the HTTP response status code.
[GetContentAsync](#getcontentasync) | Gets the response content stream asynchronously.

## Properties

### Headers

> readonly  [CoreWebView2HttpResponseHeaders](corewebview2httpresponseheaders.md) Headers

Gets the HTTP response headers as received.

### ReasonPhrase

> readonly  string ReasonPhrase

Gets the HTTP response reason phrase.

### StatusCode

> readonly  int StatusCode

Gets the HTTP response status code.



## Methods

### GetContentAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;[IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream)&gt; GetContentAsync()

Gets the response content stream asynchronously.
A `null` stream means no content was found. Note content (if any) for redirect responses is ignored.
This method returns `null` if content size is more than 123MB. If `msWebView2EnableDownloadContentInWebResourceResponseReceived` feature flag is disabled, for navigations that become downloads or if response is downloadable content type (e.g., application/octet-stream), this method also returns `null`. See [CoreWebView2.DownloadStarting](corewebview2.md#downloadstarting) event to handle the response or enable the feature flag. The Stream object that is returned will be thread-safe and as reads will be blocking while waiting for data to be available, it is recommended to read from a background thread.
If this method is being called again before a first call has completed, it will complete at the same time all prior calls do.
If this method is being called after a first call has completed, it will return immediately (asynchronously).






## Referenced by

- [CoreWebView2WebResourceResponseReceivedEventArgs](corewebview2webresourceresponsereceivedeventargs.md)
