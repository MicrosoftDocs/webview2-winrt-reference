---
description: 
title: CoreWebView2CookieManager
ms.date: 10/16/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2CookieManager
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- Microsoft.Web.WebView2.Core.CoreWebView2CookieManager
- Microsoft.Web.WebView2.Core.CoreWebView2CookieManager.AddOrUpdateCookie
- Microsoft.Web.WebView2.Core.CoreWebView2CookieManager.CopyCookie
- Microsoft.Web.WebView2.Core.CoreWebView2CookieManager.CreateCookie
- Microsoft.Web.WebView2.Core.CoreWebView2CookieManager.DeleteAllCookies
- Microsoft.Web.WebView2.Core.CoreWebView2CookieManager.DeleteCookie
- Microsoft.Web.WebView2.Core.CoreWebView2CookieManager.DeleteCookies
- Microsoft.Web.WebView2.Core.CoreWebView2CookieManager.DeleteCookiesWithDomainAndPath
- Microsoft.Web.WebView2.Core.CoreWebView2CookieManager.GetCookiesAsync
---

# CoreWebView2CookieManager Class



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

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;[`IVectorView`](/uwp/api/Windows.Foundation.Collections.IVectorView-1)&lt;[CoreWebView2Cookie](corewebview2cookie.md)&gt;&gt; GetCookiesAsync(string uri)






## Referenced by

- [CoreWebView2](corewebview2.md)
- [CoreWebView2Profile](corewebview2profile.md)
