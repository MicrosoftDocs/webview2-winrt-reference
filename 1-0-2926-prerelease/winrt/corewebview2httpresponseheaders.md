---
title: CoreWebView2HttpResponseHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/01/2024
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2HttpResponseHeaders
---

# runtimeClass CoreWebView2HttpResponseHeaders

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
