---
description: Creates, adds or updates, gets, or or view the cookies.
title: CoreWebView2CookieManager
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/16/2021
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2CookieManager
---

# runtimeclass CoreWebView2CookieManager



Creates, adds or updates, gets, or or view the cookies.

The changes would apply to the context of the user profile. That is, other WebViews under the same user profile could be affected.

## Summary

Members|Description
--|--
[AddOrUpdateCookie](#addorupdatecookie) | Adds or updates a cookie with the given cookie data; may overwrite cookies with matching name, domain, and path if they exist.
[CopyCookie](#copycookie) | Creates a cookie whose params matches those of the specified cookie.
[CreateCookie](#createcookie) | Creates a cookie object with a specified name, value, domain, and path.
[DeleteAllCookies](#deleteallcookies) | Deletes all cookies under the same profile.
[DeleteCookie](#deletecookie) | Deletes a cookie whose name and domain/path pair match those of the specified cookie.
[DeleteCookies](#deletecookies) | Deletes cookies with matching name and uri.
[DeleteCookiesWithDomainAndPath](#deletecookieswithdomainandpath) | Deletes cookies with matching name and domain/path pair.



## Methods

### AddOrUpdateCookie

> void AddOrUpdateCookie([CoreWebView2Cookie](corewebview2cookie.md) cookie)

Adds or updates a cookie with the given cookie data; may overwrite cookies with matching name, domain, and path if they exist.
`cookie` is the [CoreWebView2Cookie](corewebview2cookie.md) to be added or updated.

This method will fail if the domain of the given cookie is not specified.



### CopyCookie

> [CoreWebView2Cookie](corewebview2cookie.md) CopyCookie([CoreWebView2Cookie](corewebview2cookie.md) cookieParam)

Creates a cookie whose params matches those of the specified cookie.



### CreateCookie

> [CoreWebView2Cookie](corewebview2cookie.md) CreateCookie(string name, string value, string Domain, string Path)

Creates a cookie object with a specified name, value, domain, and path.

One can set other optional properties after cookie creation. This only creates a cookie object and it is not added to the cookie manager until you call [CoreWebView2CookieManager.AddOrUpdateCookie](corewebview2cookiemanager.md#addorupdatecookie). name that starts with whitespace(s) is not allowed.
`name` is the name for the [CoreWebView2Cookie](corewebview2cookie.md) to be created. It cannot start with whitespace(s).



### DeleteAllCookies

> void DeleteAllCookies()

Deletes all cookies under the same profile.

This could affect other WebViews under the same user profile.



### DeleteCookie

> void DeleteCookie([CoreWebView2Cookie](corewebview2cookie.md) cookie)

Deletes a cookie whose name and domain/path pair match those of the specified cookie.



### DeleteCookies

> void DeleteCookies(string name, string uri)

Deletes cookies with matching name and uri.
`name` is the name for the cookies to be deleted is required.
If `uri` is specified, deletes all cookies with the given name where domain and path match provided URI.



### DeleteCookiesWithDomainAndPath

> void DeleteCookiesWithDomainAndPath(string name, string Domain, string Path)

Deletes cookies with matching name and domain/path pair.
`name` is the name for the cookies to be deleted is required.
If `Domain` is specified, deletes only cookies with the exact domain.
If `Path` is specified, deletes only cookies with the exact path.






## Referenced by

- [CoreWebView2](corewebview2.md)
