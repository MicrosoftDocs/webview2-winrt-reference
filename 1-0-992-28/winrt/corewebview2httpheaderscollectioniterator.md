---
description: Iterator for a collection of HTTP headers.
title: CoreWebView2HttpHeadersCollectionIterator
ms.date: 09/28/2021
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2HttpHeadersCollectionIterator
---

# CoreWebView2HttpHeadersCollectionIterator Class

Implements: [IIterator](/uwp/api/Windows.Foundation.Collections.IIterator-1)&lt;[`IKeyValuePair`](/uwp/api/Windows.Foundation.Collections.IKeyValuePair-2)&lt;string, string&gt;&gt;

Iterator for a collection of HTTP headers.

## Summary

Members|Description
--|--
[Current](#current) | 
[HasCurrent](#hascurrent) | 
[GetMany](#getmany) | 
[MoveNext](#movenext) | 

## Properties

### Current

> readonly  [`IKeyValuePair`](/uwp/api/Windows.Foundation.Collections.IKeyValuePair-2)&lt;string, string&gt; Current

### HasCurrent

> readonly  bool HasCurrent



## Methods

### GetMany

> uint32_t GetMany([`IKeyValuePair`](/uwp/api/Windows.Foundation.Collections.IKeyValuePair-2)&lt;string, string&gt; items)



### MoveNext

> bool MoveNext()






## Referenced by

- [CoreWebView2HttpRequestHeaders](corewebview2httprequestheaders.md)
- [CoreWebView2HttpResponseHeaders](corewebview2httpresponseheaders.md)
