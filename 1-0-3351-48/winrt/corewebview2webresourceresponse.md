---
description: An HTTP response used with the CoreWebView2.WebResourceRequested event.
title: CoreWebView2WebResourceResponse
ms.date: 06/23/2025
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2WebResourceResponse
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2WebResourceResponse
- CoreWebView2WebResourceResponse.Content
- CoreWebView2WebResourceResponse.Headers
- CoreWebView2WebResourceResponse.ReasonPhrase
- CoreWebView2WebResourceResponse.StatusCode
---

# CoreWebView2WebResourceResponse Class



An HTTP response used with the [CoreWebView2.WebResourceRequested](corewebview2.md#webresourcerequested) event.

## Summary

Members|Description
--|--
[Content](#content) | Gets HTTP response content as stream.
[Headers](#headers) | Gets the overridden HTTP response headers.
[ReasonPhrase](#reasonphrase) | Gets or sets the HTTP response reason phrase.
[StatusCode](#statuscode) | Gets or sets the HTTP response status code.

## Properties

### Content

>  [IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) Content

Gets HTTP response content as stream.
Stream must have all the content data available by the time the [CoreWebView2.WebResourceRequested](corewebview2.md#webresourcerequested) event deferral of this response is completed. Stream should be agile or be created from a background thread to prevent performance impact to the UI thread. `null` means no content data.
When providing the response data, you should consider relevant HTTP request headers just like an HTTP server would do. For example, if the request was for a video resource in a HTML video element, the request may contain the [Range](https://developer.mozilla.org/docs/Web/HTTP/Headers/Range) header to request only a part of the video that is streaming. In this case, your response stream should be only the portion of the video specified by the range HTTP request headers and you should set the appropriate [Content-Range](https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Range) header in the response.

### Headers

> readonly  [CoreWebView2HttpResponseHeaders](corewebview2httpresponseheaders.md) Headers

Gets the overridden HTTP response headers.

### ReasonPhrase

>  string ReasonPhrase

Gets or sets the HTTP response reason phrase.

### StatusCode

>  int StatusCode

Gets or sets the HTTP response status code.






## Referenced by

- [CoreWebView2Environment](corewebview2environment.md)
- [CoreWebView2WebResourceRequestedEventArgs](corewebview2webresourcerequestedeventargs.md)
