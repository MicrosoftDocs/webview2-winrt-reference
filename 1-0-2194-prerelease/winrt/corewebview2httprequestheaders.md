---
description: 
title: CoreWebView2HttpRequestHeaders
ms.date: 11/06/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2HttpRequestHeaders
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- Microsoft.Web.WebView2.Core.CoreWebView2HttpRequestHeaders
- Microsoft.Web.WebView2.Core.CoreWebView2HttpRequestHeaders.Contains
- Microsoft.Web.WebView2.Core.CoreWebView2HttpRequestHeaders.First
- Microsoft.Web.WebView2.Core.CoreWebView2HttpRequestHeaders.GetHeader
- Microsoft.Web.WebView2.Core.CoreWebView2HttpRequestHeaders.GetHeaders
- Microsoft.Web.WebView2.Core.CoreWebView2HttpRequestHeaders.RemoveHeader
- Microsoft.Web.WebView2.Core.CoreWebView2HttpRequestHeaders.SetHeader
---

# CoreWebView2HttpRequestHeaders Class

Implements: [IIterable](/uwp/api/Windows.Foundation.Collections.IIterable-1)&lt;[`IKeyValuePair`](/uwp/api/Windows.Foundation.Collections.IKeyValuePair-2)&lt;string, string&gt;&gt;

## Summary

Members|Description
--|--
[Contains](#contains) | 
[First](#first) | 
[GetHeader](#getheader) | 
[GetHeaders](#getheaders) | 
[RemoveHeader](#removeheader) | 
[SetHeader](#setheader) | 



## Methods

### Contains

> bool Contains(string name)



### First

> [`IIterator`](/uwp/api/Windows.Foundation.Collections.IIterator-1)&lt;[`IKeyValuePair`](/uwp/api/Windows.Foundation.Collections.IKeyValuePair-2)&lt;string, string&gt;&gt; First()



### GetHeader

> string GetHeader(string name)



### GetHeaders

> [CoreWebView2HttpHeadersCollectionIterator](corewebview2httpheaderscollectioniterator.md) GetHeaders(string name)



### RemoveHeader

> void RemoveHeader(string name)



### SetHeader

> void SetHeader(string name, string value)






## Referenced by

- [CoreWebView2NavigationStartingEventArgs](corewebview2navigationstartingeventargs.md)
- [CoreWebView2WebResourceRequest](corewebview2webresourcerequest.md)
