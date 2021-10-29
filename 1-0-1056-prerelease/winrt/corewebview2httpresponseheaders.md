---
description: HTTP response headers.
title: CoreWebView2HttpResponseHeaders
ms.date: 10/28/2021
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2HttpResponseHeaders
---

# CoreWebView2HttpResponseHeaders Class

Implements: [IIterable](/uwp/api/Windows.Foundation.Collections.IIterable-1)&lt;[`IKeyValuePair`](/uwp/api/Windows.Foundation.Collections.IKeyValuePair-2)&lt;string, string&gt;&gt;

HTTP response headers.
Used to construct a [CoreWebView2WebResourceResponse](corewebview2webresourceresponse.md) for the [CoreWebView2.WebResourceRequested](corewebview2.md#webresourcerequested) event.

## Summary

Members|Description
--|--
[AppendHeader](#appendheader) | Appends header line with name and value.
[Contains](#contains) | Checks whether this CoreWebView2HttpResponseHeaders contain entries matching the header name.
[First](#first) | 
[GetHeader](#getheader) | Gets the first header value in the collection matching the name.
[GetHeaders](#getheaders) | Gets the header values matching the name.



## Methods

### AppendHeader

> void AppendHeader(string name, string value)

Appends header line with name and value.



### Contains

> bool Contains(string name)

Checks whether this CoreWebView2HttpResponseHeaders contain entries matching the header name.



### First

> [`IIterator`](/uwp/api/Windows.Foundation.Collections.IIterator-1)&lt;[`IKeyValuePair`](/uwp/api/Windows.Foundation.Collections.IKeyValuePair-2)&lt;string, string&gt;&gt; First()



### GetHeader

> string GetHeader(string name)

Gets the first header value in the collection matching the name.



### GetHeaders

> [CoreWebView2HttpHeadersCollectionIterator](corewebview2httpheaderscollectioniterator.md) GetHeaders(string name)

Gets the header values matching the name.






## Referenced by

- [CoreWebView2WebResourceResponse](corewebview2webresourceresponse.md)
- [CoreWebView2WebResourceResponseView](corewebview2webresourceresponseview.md)
