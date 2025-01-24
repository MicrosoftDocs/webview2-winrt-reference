---
description: HTTP request headers.
title: CoreWebView2HttpRequestHeaders
ms.date: 01/16/2025
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2HttpRequestHeaders
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2HttpRequestHeaders
- CoreWebView2HttpRequestHeaders.Contains
- CoreWebView2HttpRequestHeaders.First
- CoreWebView2HttpRequestHeaders.GetHeader
- CoreWebView2HttpRequestHeaders.GetHeaders
- CoreWebView2HttpRequestHeaders.RemoveHeader
- CoreWebView2HttpRequestHeaders.SetHeader
---

# CoreWebView2HttpRequestHeaders Class

Implements: [IIterable](/uwp/api/Windows.Foundation.Collections.IIterable-1)&lt;[`IKeyValuePair`](/uwp/api/Windows.Foundation.Collections.IKeyValuePair-2)&lt;string, string&gt;&gt;

HTTP request headers.
Used to inspect the HTTP request on [CoreWebView2.WebResourceRequested](corewebview2.md#webresourcerequested) event and [CoreWebView2.NavigationStarting](corewebview2.md#navigationstarting) event. It is possible to modify the HTTP request headers from a [CoreWebView2.WebResourceRequested](corewebview2.md#webresourcerequested) event, but not from a [CoreWebView2.NavigationStarting](corewebview2.md#navigationstarting) event.

## Summary

Members|Description
--|--
[Contains](#contains) | Checks whether the headers contain an entry that matches the header name.
[First](#first) | 
[GetHeader](#getheader) | Gets the header value matching the name.
[GetHeaders](#getheaders) | Gets the header value matching the name using a [CoreWebView2HttpHeadersCollectionIterator](corewebview2httpheaderscollectioniterator.md).
[RemoveHeader](#removeheader) | Removes header that matches the name.
[SetHeader](#setheader) | Adds or updates header that matches the name.



## Methods

### Contains

> bool Contains(string name)

Checks whether the headers contain an entry that matches the header name.



### First

> [`IIterator`](/uwp/api/Windows.Foundation.Collections.IIterator-1)&lt;[`IKeyValuePair`](/uwp/api/Windows.Foundation.Collections.IKeyValuePair-2)&lt;string, string&gt;&gt; First()



### GetHeader

> string GetHeader(string name)

Gets the header value matching the name.



### GetHeaders

> [CoreWebView2HttpHeadersCollectionIterator](corewebview2httpheaderscollectioniterator.md) GetHeaders(string name)

Gets the header value matching the name using a [CoreWebView2HttpHeadersCollectionIterator](corewebview2httpheaderscollectioniterator.md).



### RemoveHeader

> void RemoveHeader(string name)

Removes header that matches the name.



### SetHeader

> void SetHeader(string name, string value)

Adds or updates header that matches the name.






## Referenced by

- [CoreWebView2NavigationStartingEventArgs](corewebview2navigationstartingeventargs.md)
- [CoreWebView2WebResourceRequest](corewebview2webresourcerequest.md)
