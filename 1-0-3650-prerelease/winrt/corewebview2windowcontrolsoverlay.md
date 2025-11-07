---
description: Provides methods and properties which allows you to enable and configure the WebView2 Window Controls Overlay. The Overlay is a region on the top right/left of the webview window which contains the caption buttons (minimize, maximize, restore, close). Enabling the Overlay allows for custom app title bars to be rendered completely inside the webview window.
title: CoreWebView2WindowControlsOverlay
ms.date: 11/03/2025
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



Provides methods and properties which allows you to enable and configure the WebView2 Window Controls Overlay. The Overlay is a region on the top right/left of the webview window which contains the caption buttons (minimize, maximize, restore, close). Enabling the Overlay allows for custom app title bars to be rendered completely inside the webview window.

This API is designed to be used in addition with the other non-client region APIs and features. These include `app-region: drag`, and `IsNonClientRegionSupportEnabled`.


## Summary

Members|Description
--|--
[BackgroundColor](#backgroundcolor) | The `BackgroundColor` property allows you to set a background color for the overlay. Based on the background color you choose, WebView2 will automatically calculate a foreground and hover color. Defaults to #f3f3f3. This API supports transparency.
[Height](#height) | The `Height` property in raw screen pixels, allows you to set the height of the overlay and title bar area. Defaults to 48px. There is no minimum height restriction for this API, so it is up to the developer to make sure that the height of your window controls overlay is enough that users can see and interact with it. We recommend using GetSystemMetrics(SM_CYCAPTION) as your minimum height.
[IsEnabled](#isenabled) | The `IsEnabled` property allows you to opt in to using the WebView2 window controls overlay. Defaults to `FALSE`.

## Properties

### BackgroundColor

>  [Color](/uwp/api/Windows.UI.Color) BackgroundColor

The `BackgroundColor` property allows you to set a background color for the overlay. Based on the background color you choose, WebView2 will automatically calculate a foreground and hover color. Defaults to #f3f3f3. This API supports transparency.

### Height

>  uint32_t Height

The `Height` property in raw screen pixels, allows you to set the height of the overlay and title bar area. Defaults to 48px. There is no minimum height restriction for this API, so it is up to the developer to make sure that the height of your window controls overlay is enough that users can see and interact with it. We recommend using GetSystemMetrics(SM_CYCAPTION) as your minimum height.


### IsEnabled

>  bool IsEnabled

The `IsEnabled` property allows you to opt in to using the WebView2 window controls overlay. Defaults to `FALSE`.

When this property is `TRUE`, WebView2 will draw its own minimize, maximize, and close buttons on the top right corner of the WebView2. 

When using this you should configure your app window to not display its default window control buttons. You are responsible for creating a title bar for your app by using the available space to the left of the controls overlay. In doing so, you can utilize the [IsNonClientRegionSupportEnabled](https://learn.microsoft.com/en-us/microsoft-edge/webview2/reference/win32/icorewebview2settings9?view=webview2-1.0.2739.15) API to enable draggable regions for your custom title bar.

The Overlay buttons will cover the HTML content, and will prevent mouse interactions with any elements directly below it, so you should avoid placing content there. To that end, there are four [CSS environment variables](https://developer.mozilla.org/en-US/docs/Web/API/Window_Controls_Overlay_API#css_environment_variables) titlebar-area-x, titlebar-area-y, titlebar-area-width, titlebar-area-height defined to help you get the dimensions of the available titlebar area to the left of the overlay. Similarly the navigator object will contain a [WindowControlsOverlay property](https://developer.mozilla.org/en-US/docs/Web/API/WindowControlsOverlay) which can be used to get the titlebar area as a rect, and listen for changes to the size of that area.







## Referenced by

- [CoreWebView2](corewebview2.md)
