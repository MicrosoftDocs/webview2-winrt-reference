---
description: An HTTP request used with the CoreWebView2.WebResourceRequested event.
title: CoreWebView2WebResourceRequest
ms.date: 05/20/2024
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2WebResourceRequest
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- Microsoft.Web.WebView2.Core.CoreWebView2WebResourceRequest
- Microsoft.Web.WebView2.Core.CoreWebView2WebResourceRequest.Content
- Microsoft.Web.WebView2.Core.CoreWebView2WebResourceRequest.Headers
- Microsoft.Web.WebView2.Core.CoreWebView2WebResourceRequest.Method
- Microsoft.Web.WebView2.Core.CoreWebView2WebResourceRequest.Uri
- Microsoft.Web.WebView2.Core.CoreWebView2WebResourceRequest.get_Content
- Microsoft.Web.WebView2.Core.CoreWebView2WebResourceRequest.get_Headers
- Microsoft.Web.WebView2.Core.CoreWebView2WebResourceRequest.get_Method
- Microsoft.Web.WebView2.Core.CoreWebView2WebResourceRequest.get_Uri
- Microsoft.Web.WebView2.Core.CoreWebView2WebResourceRequest.put_Content
- Microsoft.Web.WebView2.Core.CoreWebView2WebResourceRequest.put_Method
- Microsoft.Web.WebView2.Core.CoreWebView2WebResourceRequest.put_Uri
---

# CoreWebView2WebResourceRequest Class



An HTTP request used with the [CoreWebView2.WebResourceRequested](corewebview2.md#webresourcerequested) event.

## Summary

Members|Description
--|--
[Content](#content) | Gets or sets the HTTP request message body as stream.
[Headers](#headers) | Gets the mutable HTTP request headers.
[Method](#method) | Gets or sets the HTTP request method.
[Uri](#uri) | Gets or sets the request URI.

## Properties

### Content

>  [IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) Content

Gets or sets the HTTP request message body as stream.
POST data should be here. If a stream is set, which overrides the message body, the stream must have all the content data available by the time the [CoreWebView2.WebResourceRequested](corewebview2.md#webresourcerequested) event deferral of this request is completed. Stream should be agile or be created from a background STA to prevent performance impact to the UI thread. `null` means no content data.

### Headers

> readonly  [CoreWebView2HttpRequestHeaders](corewebview2httprequestheaders.md) Headers

Gets the mutable HTTP request headers.

### Method

>  string Method

Gets or sets the HTTP request method.

### Uri

>  string Uri

Gets or sets the request URI.






## Referenced by

- [CoreWebView2](corewebview2.md)
- [CoreWebView2Environment](corewebview2environment.md)
- [CoreWebView2WebResourceRequestedEventArgs](corewebview2webresourcerequestedeventargs.md)
- [CoreWebView2WebResourceResponseReceivedEventArgs](corewebview2webresourceresponsereceivedeventargs.md)
