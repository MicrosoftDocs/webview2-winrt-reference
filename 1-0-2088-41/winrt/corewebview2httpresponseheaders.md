---
description: 
title: CoreWebView2HttpResponseHeaders
ms.date: 10/16/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2HttpResponseHeaders
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- Microsoft.Web.WebView2.Core.CoreWebView2HttpResponseHeaders
- Microsoft.Web.WebView2.Core.CoreWebView2HttpResponseHeaders.AppendHeader
- Microsoft.Web.WebView2.Core.CoreWebView2HttpResponseHeaders.Contains
- Microsoft.Web.WebView2.Core.CoreWebView2HttpResponseHeaders.First
- Microsoft.Web.WebView2.Core.CoreWebView2HttpResponseHeaders.GetHeader
- Microsoft.Web.WebView2.Core.CoreWebView2HttpResponseHeaders.GetHeaders
---

# CoreWebView2HttpResponseHeaders Class

Implements: [IIterable](/uwp/api/Windows.Foundation.Collections.IIterable-1)&lt;[`IKeyValuePair`](/uwp/api/Windows.Foundation.Collections.IKeyValuePair-2)&lt;string, string&gt;&gt;

## Summary

Members|Description
--|--
[AppendHeader](#appendheader) | 
[Contains](#contains) | 
[First](#first) | 
[GetHeader](#getheader) | 
[GetHeaders](#getheaders) | 



## Methods

### AppendHeader

> void AppendHeader(string name, string value)



### Contains

> bool Contains(string name)



### First

> [`IIterator`](/uwp/api/Windows.Foundation.Collections.IIterator-1)&lt;[`IKeyValuePair`](/uwp/api/Windows.Foundation.Collections.IKeyValuePair-2)&lt;string, string&gt;&gt; First()



### GetHeader

> string GetHeader(string name)



### GetHeaders

> [CoreWebView2HttpHeadersCollectionIterator](corewebview2httpheaderscollectioniterator.md) GetHeaders(string name)






## Referenced by

- [CoreWebView2WebResourceResponse](corewebview2webresourceresponse.md)
- [CoreWebView2WebResourceResponseView](corewebview2webresourceresponseview.md)
