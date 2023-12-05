---
description: Browser extension installed on current profile.
title: CoreWebView2BrowserExtension
ms.date: 12/11/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2BrowserExtension
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- Microsoft.Web.WebView2.Core.CoreWebView2BrowserExtension
- Microsoft.Web.WebView2.Core.CoreWebView2BrowserExtension.Id
- Microsoft.Web.WebView2.Core.CoreWebView2BrowserExtension.IsEnabled
- Microsoft.Web.WebView2.Core.CoreWebView2BrowserExtension.Name
- Microsoft.Web.WebView2.Core.CoreWebView2BrowserExtension.EnableAsync
- Microsoft.Web.WebView2.Core.CoreWebView2BrowserExtension.RemoveAsync
- Microsoft.Web.WebView2.Core.CoreWebView2BrowserExtension.get_Id
- Microsoft.Web.WebView2.Core.CoreWebView2BrowserExtension.get_IsEnabled
- Microsoft.Web.WebView2.Core.CoreWebView2BrowserExtension.get_Name
---

# CoreWebView2BrowserExtension Class



Browser extension installed on current profile.

## Summary

Members|Description
--|--
[Id](#id) | This is the browser extension's ID. This is the same browser extension ID returned by the browser extension API [chrome.runtime.id](https://developer.mozilla.org/en-US/docs/Mozilla/Add-ons/WebExtensions/API/runtime/id). Please see that documentation for more details on how the ID is generated. After an extension is removed, calling `Id` will return the id of the extension that is removed.
[IsEnabled](#isenabled) | If `IsEnabled` is true then the Extension is enabled and running in WebView instances. If it is false then the Extension is disabled and not running in WebView instances. When a Extension is first installed, `IsEnable` are default to be `true`. `IsEnabled` is persisted per profile. After an extension is removed, calling `IsEnabled` will return the value at the time it was removed.
[Name](#name) | This is the browser extension's name. This value is defined in this browser extension's manifest.json file. If manifest.json define extension's localized name, this value will be the localized version of the name. Please see [Manifest.json name](https://developer.mozilla.org/en-US/docs/Mozilla/Add-ons/WebExtensions/manifest.json/name) for more details.
[EnableAsync](#enableasync) | Sets whether this browser extension is enabled or disabled. This change applies immediately to the extension in all HTML documents in all WebView2s associated with this profile. After an extension is removed, calling `Enable` will not change the value of `IsEnabled`.
[RemoveAsync](#removeasync) | Removes this browser extension from its WebView2 Profile. The browser extension is removed immediately including from all currently running HTML documents associated with this WebView2 Profile. The removal is persisted and future uses of this profile will not have this extension installed. After an extension is removed, calling `Remove` again will cause an exception.

## Properties

### Id

> readonly  string Id

This is the browser extension's ID. This is the same browser extension ID returned by the browser extension API [chrome.runtime.id](https://developer.mozilla.org/en-US/docs/Mozilla/Add-ons/WebExtensions/API/runtime/id). Please see that documentation for more details on how the ID is generated. After an extension is removed, calling `Id` will return the id of the extension that is removed.

### IsEnabled

> readonly  bool IsEnabled

If `IsEnabled` is true then the Extension is enabled and running in WebView instances. If it is false then the Extension is disabled and not running in WebView instances. When a Extension is first installed, `IsEnable` are default to be `true`. `IsEnabled` is persisted per profile. After an extension is removed, calling `IsEnabled` will return the value at the time it was removed.

### Name

> readonly  string Name

This is the browser extension's name. This value is defined in this browser extension's manifest.json file. If manifest.json define extension's localized name, this value will be the localized version of the name. Please see [Manifest.json name](https://developer.mozilla.org/en-US/docs/Mozilla/Add-ons/WebExtensions/manifest.json/name) for more details.



## Methods

### EnableAsync

> [IAsyncAction](/uwp/api/Windows.Foundation.IAsyncAction) EnableAsync(bool IsEnabled)

Sets whether this browser extension is enabled or disabled. This change applies immediately to the extension in all HTML documents in all WebView2s associated with this profile. After an extension is removed, calling `Enable` will not change the value of `IsEnabled`.



### RemoveAsync

> [IAsyncAction](/uwp/api/Windows.Foundation.IAsyncAction) RemoveAsync()

Removes this browser extension from its WebView2 Profile. The browser extension is removed immediately including from all currently running HTML documents associated with this WebView2 Profile. The removal is persisted and future uses of this profile will not have this extension installed. After an extension is removed, calling `Remove` again will cause an exception.




