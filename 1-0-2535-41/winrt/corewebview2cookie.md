---
description: Provides a set of properties that are used to manage a CoreWebView2Cookie.
title: CoreWebView2Cookie
ms.date: 05/28/2024
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2Cookie
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- Microsoft.Web.WebView2.Core.CoreWebView2Cookie
- Microsoft.Web.WebView2.Core.CoreWebView2Cookie.Domain
- Microsoft.Web.WebView2.Core.CoreWebView2Cookie.Expires
- Microsoft.Web.WebView2.Core.CoreWebView2Cookie.IsHttpOnly
- Microsoft.Web.WebView2.Core.CoreWebView2Cookie.IsSecure
- Microsoft.Web.WebView2.Core.CoreWebView2Cookie.IsSession
- Microsoft.Web.WebView2.Core.CoreWebView2Cookie.Name
- Microsoft.Web.WebView2.Core.CoreWebView2Cookie.Path
- Microsoft.Web.WebView2.Core.CoreWebView2Cookie.SameSite
- Microsoft.Web.WebView2.Core.CoreWebView2Cookie.Value
- Microsoft.Web.WebView2.Core.CoreWebView2Cookie.get_Domain
- Microsoft.Web.WebView2.Core.CoreWebView2Cookie.get_Expires
- Microsoft.Web.WebView2.Core.CoreWebView2Cookie.get_IsHttpOnly
- Microsoft.Web.WebView2.Core.CoreWebView2Cookie.get_IsSecure
- Microsoft.Web.WebView2.Core.CoreWebView2Cookie.get_IsSession
- Microsoft.Web.WebView2.Core.CoreWebView2Cookie.get_Name
- Microsoft.Web.WebView2.Core.CoreWebView2Cookie.get_Path
- Microsoft.Web.WebView2.Core.CoreWebView2Cookie.get_SameSite
- Microsoft.Web.WebView2.Core.CoreWebView2Cookie.get_Value
- Microsoft.Web.WebView2.Core.CoreWebView2Cookie.put_Expires
- Microsoft.Web.WebView2.Core.CoreWebView2Cookie.put_IsHttpOnly
- Microsoft.Web.WebView2.Core.CoreWebView2Cookie.put_IsSecure
- Microsoft.Web.WebView2.Core.CoreWebView2Cookie.put_SameSite
- Microsoft.Web.WebView2.Core.CoreWebView2Cookie.put_Value
---

# CoreWebView2Cookie Class



Provides a set of properties that are used to manage a CoreWebView2Cookie.

## Summary

Members|Description
--|--
[Domain](#domain) | Gets the domain for which the cookie is valid.
[Expires](#expires) | The expiration date and time for the cookie since the UNIX epoch.
[IsHttpOnly](#ishttponly) | Determines whether this cookie is http-only.
[IsSecure](#issecure) | Gets or sets the security level of this cookie.
[IsSession](#issession) | Determines whether this is a session cookie. The default value is `false`.
[Name](#name) | Get or sets the cookie name.
[Path](#path) | Gets the path for which the cookie is valid.
[SameSite](#samesite) | Determines the SameSite status of the cookie which represents the enforcement mode of the cookie.
[Value](#value) | Gets or sets the cookie value.

## Properties

### Domain

> readonly  string Domain

Gets the domain for which the cookie is valid.
The default value is the host that this cookie has been received from. Note that, for instance, `.bing.com`, `bing.com`, and `www.bing.com` are considered different domains.

### Expires

>  double Expires

The expiration date and time for the cookie since the UNIX epoch.

### IsHttpOnly

>  bool IsHttpOnly

Determines whether this cookie is http-only.

### IsSecure

>  bool IsSecure

Gets or sets the security level of this cookie.

### IsSession

> readonly  bool IsSession

Determines whether this is a session cookie. The default value is `false`.

### Name

> readonly  string Name

Get or sets the cookie name.

### Path

> readonly  string Path

Gets the path for which the cookie is valid.
The default value is "/", which means this cookie will be sent to all pages on the [CoreWebView2Cookie.Domain](corewebview2cookie.md#domain).

### SameSite

>  [CoreWebView2CookieSameSiteKind](corewebview2cookiesamesitekind.md) SameSite

Determines the SameSite status of the cookie which represents the enforcement mode of the cookie.
The default value is [CoreWebView2CookieSameSiteKind](corewebview2cookiesamesitekind.md).Lax.

### Value

>  string Value

Gets or sets the cookie value.






## Referenced by

- [CoreWebView2CookieManager](corewebview2cookiemanager.md)
