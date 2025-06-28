---
description: Provides methods and properties which allows you to enable and configure the Webview2 Window Controls Overlay. The Overlay is a region on the top right/left of the webview window which contains the caption buttons (minimize, maximize, restore, close). Enabling the Overlay allows for custom app title bars rendered completely inside the webview window.
title: CoreWebView2WindowControlsOverlay
ms.date: 06/26/2025
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2WindowControlsOverlay
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2WindowControlsOverlay
- CoreWebView2WindowControlsOverlay.BackgroundColor
- CoreWebView2WindowControlsOverlay.Height
- CoreWebView2WindowControlsOverlay.IsEnabled
---

# CoreWebView2WindowControlsOverlay Class



Provides methods and properties which allows you to enable and configure the Webview2 Window Controls Overlay. The Overlay is a region on the top right/left of the webview window which contains the caption buttons (minimize, maximize, restore, close). Enabling the Overlay allows for custom app title bars rendered completely inside the webview window.

This API is designed to be used in addition with the other non-client region APIs and features. These include `app-region: drag`, and `IsNonClientRegionSupportEnabled`.


## Summary

Members|Description
--|--
[BackgroundColor](#backgroundcolor) | The `BackgroundColor` property allows you to set a background color for the overlay. Based on the background color you choose, Webview2 will automatically calculate a foreground and hover color. Defaults to #f3f3f3. This API supports transparency.
[Height](#height) | The `Height` property in raw screen pixels, allows you to set the height of the overlay and title bar area. Defaults to 48px. There is no minimum height restriction for this API, so it is up to the developer to make sure that the height of your window controls overlay is enough that users can see and interact with it. We recommend using GetSystemMetrics(SM_CYCAPTION) as your minimum height.
[IsEnabled](#isenabled) | 

## Properties

### BackgroundColor

>  [Color](/uwp/api/Windows.UI.Color) BackgroundColor

The `BackgroundColor` property allows you to set a background color for the overlay. Based on the background color you choose, Webview2 will automatically calculate a foreground and hover color. Defaults to #f3f3f3. This API supports transparency.

### Height

>  uint32_t Height

The `Height` property in raw screen pixels, allows you to set the height of the overlay and title bar area. Defaults to 48px. There is no minimum height restriction for this API, so it is up to the developer to make sure that the height of your window controls overlay is enough that users can see and interact with it. We recommend using GetSystemMetrics(SM_CYCAPTION) as your minimum height.


### IsEnabled

>  bool IsEnabled






## Referenced by

- [CoreWebView2](corewebview2.md)
