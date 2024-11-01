---
title: CoreWebView2CookieManager
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/01/2024
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2CookieManager
---

# runtimeClass CoreWebView2CookieManager



## Summary

Members|Description
--|--
[AddOrUpdateCookie](#addorupdatecookie) | 
[CopyCookie](#copycookie) | 
[CreateCookie](#createcookie) | 
[DeleteAllCookies](#deleteallcookies) | 
[DeleteCookie](#deletecookie) | 
[DeleteCookies](#deletecookies) | 
[DeleteCookiesWithDomainAndPath](#deletecookieswithdomainandpath) | 
[GetCookiesAsync](#getcookiesasync) | 



## Methods

### AddOrUpdateCookie

> void AddOrUpdateCookie([CoreWebView2Cookie](corewebview2cookie.md) cookie)



### CopyCookie

> [CoreWebView2Cookie](corewebview2cookie.md) CopyCookie([CoreWebView2Cookie](corewebview2cookie.md) cookieParam)



### CreateCookie

> [CoreWebView2Cookie](corewebview2cookie.md) CreateCookie(string name, string value, string Domain, string Path)



### DeleteAllCookies

> void DeleteAllCookies()



### DeleteCookie

> void DeleteCookie([CoreWebView2Cookie](corewebview2cookie.md) cookie)



### DeleteCookies

> void DeleteCookies(string name, string uri)



### DeleteCookiesWithDomainAndPath

> void DeleteCookiesWithDomainAndPath(string name, string Domain, string Path)



### GetCookiesAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;[`IVectorView`](/uwp/api/Windows.Foundation.Collections.IVectorView-1)&lt;[CoreWebView2Cookie](corewebview2cookie.md)&gt;&gt; GetCookiesAsync(string operation)






## Referenced by

- [CoreWebView2](corewebview2.md)
- [CoreWebView2Profile](corewebview2profile.md)
