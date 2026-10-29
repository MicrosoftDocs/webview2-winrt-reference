---
description: Browser extension installed on current profile.
title: CoreWebView2BrowserExtension
ms.date: 10-29-2026
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2BrowserExtension
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2BrowserExtension
- CoreWebView2BrowserExtension.Id
- CoreWebView2BrowserExtension.IsEnabled
- CoreWebView2BrowserExtension.Name
- CoreWebView2BrowserExtension.EnableAsync
- CoreWebView2BrowserExtension.RemoveAsync
---

# CoreWebView2BrowserExtension Class



Browser extension installed on current profile.

## Summary

Members|Description
--|--
[Id](#id) | This is the browser extension's ID.
[IsEnabled](#isenabled) | If `IsEnabled` is true then the Extension is enabled and running in WebView instances.
[Name](#name) | This is the browser extension's name.
[EnableAsync](#enableasync) | Sets whether this browser extension is enabled or disabled.
[RemoveAsync](#removeasync) | Removes this browser extension from its WebView2 Profile.

## Properties

### Id

> readonly  string Id

This is the browser extension's ID.
This is the same browser extension ID returned by the browser extension API [chrome.runtime.id](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/runtime/id). Please see that documentation for more details on how the ID is generated. After an extension is removed, calling `Id` will return the id of the extension that is removed.

### IsEnabled

> readonly  bool IsEnabled

If `IsEnabled` is true then the Extension is enabled and running in WebView instances.
If it is false then the Extension is disabled and not running in WebView instances. When an Extension is first installed, `IsEnabled` defaults to `true`. `IsEnabled` is persisted per profile. After an extension is removed, calling `IsEnabled` will return the value at the time it was removed.

### Name

> readonly  string Name

This is the browser extension's name.
This value is defined in this browser extension's manifest.json file. If manifest.json defines the extension's localized name, this value will be the localized version of the name. Please see [Manifest.json name](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/name) for more details.



## Methods

### EnableAsync

> [IAsyncAction](/uwp/api/Windows.Foundation.IAsyncAction) EnableAsync(bool IsEnabled)

Sets whether this browser extension is enabled or disabled.
This change applies immediately to the extension in all HTML documents in all WebView2s associated with this profile. After an extension is removed, calling [CoreWebView2BrowserExtension.EnableAsync](corewebview2browserextension.md#enableasync) will not change the value of [CoreWebView2BrowserExtension.IsEnabled](corewebview2browserextension.md#isenabled).



### RemoveAsync

> [IAsyncAction](/uwp/api/Windows.Foundation.IAsyncAction) RemoveAsync()

Removes this browser extension from its WebView2 Profile.
The browser extension is removed immediately including from all currently running HTML documents associated with this WebView2 Profile. The removal is persisted and future uses of this profile will not have this extension installed. After an extension is removed, calling [CoreWebView2BrowserExtension.RemoveAsync](corewebview2browserextension.md#removeasync) again will cause an exception.




