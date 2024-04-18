---
description: The window features for a WebView popup window.
title: CoreWebView2WindowFeatures
ms.date: 04/22/2024
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2WindowFeatures
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- Microsoft.Web.WebView2.Core.CoreWebView2WindowFeatures
- Microsoft.Web.WebView2.Core.CoreWebView2WindowFeatures.HasPosition
- Microsoft.Web.WebView2.Core.CoreWebView2WindowFeatures.HasSize
- Microsoft.Web.WebView2.Core.CoreWebView2WindowFeatures.Height
- Microsoft.Web.WebView2.Core.CoreWebView2WindowFeatures.Left
- Microsoft.Web.WebView2.Core.CoreWebView2WindowFeatures.ShouldDisplayMenuBar
- Microsoft.Web.WebView2.Core.CoreWebView2WindowFeatures.ShouldDisplayScrollBars
- Microsoft.Web.WebView2.Core.CoreWebView2WindowFeatures.ShouldDisplayStatus
- Microsoft.Web.WebView2.Core.CoreWebView2WindowFeatures.ShouldDisplayToolbar
- Microsoft.Web.WebView2.Core.CoreWebView2WindowFeatures.Top
- Microsoft.Web.WebView2.Core.CoreWebView2WindowFeatures.Width
- Microsoft.Web.WebView2.Core.CoreWebView2WindowFeatures.get_HasPosition
- Microsoft.Web.WebView2.Core.CoreWebView2WindowFeatures.get_HasSize
- Microsoft.Web.WebView2.Core.CoreWebView2WindowFeatures.get_Height
- Microsoft.Web.WebView2.Core.CoreWebView2WindowFeatures.get_Left
- Microsoft.Web.WebView2.Core.CoreWebView2WindowFeatures.get_ShouldDisplayMenuBar
- Microsoft.Web.WebView2.Core.CoreWebView2WindowFeatures.get_ShouldDisplayScrollBars
- Microsoft.Web.WebView2.Core.CoreWebView2WindowFeatures.get_ShouldDisplayStatus
- Microsoft.Web.WebView2.Core.CoreWebView2WindowFeatures.get_ShouldDisplayToolbar
- Microsoft.Web.WebView2.Core.CoreWebView2WindowFeatures.get_Top
- Microsoft.Web.WebView2.Core.CoreWebView2WindowFeatures.get_Width
---

# CoreWebView2WindowFeatures Class



The window features for a WebView popup window.
The fields match the `windowFeatures` passed to `window.open()` as specified in [Window features](https://developer.mozilla.org/docs/Web/API/Window/open#Window_features) on MDN. There is no requirement for you to respect the values. If your app does not have corresponding UI features (for example, no toolbar) or if all instance of WebView are opened in tabs and do not have distinct size or positions, then your app does not respect the values. You may want to respect values, but perhaps only some apply to the UI of you app. Accordingly, you may respect all, some, or none of the properties as appropriate for your app. For all numeric properties, if the value that is passed to `window.open()` is outside the range of an uint, the resulting value is uint.MaxValue. If you are not able to parse the value an integer, it is considered 0. If the value is a floating point value, it is rounded down to an integer.

## Summary

Members|Description
--|--
[HasPosition](#hasposition) | Indicates whether the left and top values are specified.
[HasSize](#hassize) | Indicates whether the height and width values are specified.
[Height](#height) | Gets the height of the window. Ignored if [CoreWebView2WindowFeatures.HasSize](corewebview2windowfeatures.md#hassize) is `false`.
[Left](#left) | Gets the left position of the window. Ignored if [CoreWebView2WindowFeatures.HasPosition](corewebview2windowfeatures.md#hasposition) is `false`.
[ShouldDisplayMenuBar](#shoulddisplaymenubar) | Indicates that the menu bar is displayed.
[ShouldDisplayScrollBars](#shoulddisplayscrollbars) | Indicates that the scroll bars are displayed.
[ShouldDisplayStatus](#shoulddisplaystatus) | Indicates that the status bar is displayed.
[ShouldDisplayToolbar](#shoulddisplaytoolbar) | Indicates that the browser toolbar is displayed.
[Top](#top) | Gets the top position of the window. Ignored if [CoreWebView2WindowFeatures.HasPosition](corewebview2windowfeatures.md#hasposition) is `false`.
[Width](#width) | Gets the width of the window. Ignored if [CoreWebView2WindowFeatures.HasSize](corewebview2windowfeatures.md#hassize) is `false`.

## Properties

### HasPosition

> readonly  bool HasPosition

Indicates whether the left and top values are specified.

### HasSize

> readonly  bool HasSize

Indicates whether the height and width values are specified.

### Height

> readonly  uint32_t Height

Gets the height of the window. Ignored if [CoreWebView2WindowFeatures.HasSize](corewebview2windowfeatures.md#hassize) is `false`.

### Left

> readonly  uint32_t Left

Gets the left position of the window. Ignored if [CoreWebView2WindowFeatures.HasPosition](corewebview2windowfeatures.md#hasposition) is `false`.

### ShouldDisplayMenuBar

> readonly  bool ShouldDisplayMenuBar

Indicates that the menu bar is displayed.

### ShouldDisplayScrollBars

> readonly  bool ShouldDisplayScrollBars

Indicates that the scroll bars are displayed.

### ShouldDisplayStatus

> readonly  bool ShouldDisplayStatus

Indicates that the status bar is displayed.

### ShouldDisplayToolbar

> readonly  bool ShouldDisplayToolbar

Indicates that the browser toolbar is displayed.

### Top

> readonly  uint32_t Top

Gets the top position of the window. Ignored if [CoreWebView2WindowFeatures.HasPosition](corewebview2windowfeatures.md#hasposition) is `false`.

### Width

> readonly  uint32_t Width

Gets the width of the window. Ignored if [CoreWebView2WindowFeatures.HasSize](corewebview2windowfeatures.md#hassize) is `false`.






## Referenced by

- [CoreWebView2NewWindowRequestedEventArgs](corewebview2newwindowrequestedeventargs.md)
