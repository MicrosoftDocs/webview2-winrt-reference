---
description: An HTTP response used with the CoreWebView2.WebResourceRequested event.
title: CoreWebView2WebResourceResponse
ms.date: 08/29/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2WebResourceResponse
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- Microsoft.Web.WebView2.Core.CoreWebView2WebResourceResponse
- Microsoft.Web.WebView2.Core.CoreWebView2WebResourceResponse.Content
- Microsoft.Web.WebView2.Core.CoreWebView2WebResourceResponse.Headers
- Microsoft.Web.WebView2.Core.CoreWebView2WebResourceResponse.ReasonPhrase
- Microsoft.Web.WebView2.Core.CoreWebView2WebResourceResponse.StatusCode
- Microsoft.Web.WebView2.Core.CoreWebView2WebResourceResponse.get_Content
- Microsoft.Web.WebView2.Core.CoreWebView2WebResourceResponse.get_Headers
- Microsoft.Web.WebView2.Core.CoreWebView2WebResourceResponse.get_ReasonPhrase
- Microsoft.Web.WebView2.Core.CoreWebView2WebResourceResponse.get_StatusCode
- Microsoft.Web.WebView2.Core.CoreWebView2WebResourceResponse.put_Content
- Microsoft.Web.WebView2.Core.CoreWebView2WebResourceResponse.put_ReasonPhrase
- Microsoft.Web.WebView2.Core.CoreWebView2WebResourceResponse.put_StatusCode
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
