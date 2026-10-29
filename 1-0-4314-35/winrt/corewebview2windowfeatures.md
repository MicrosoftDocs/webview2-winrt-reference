---
description: The window features for a WebView popup window.
title: CoreWebView2WindowFeatures
ms.date: 10/29/2026
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2WindowFeatures
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2WindowFeatures
- CoreWebView2WindowFeatures.HasPosition
- CoreWebView2WindowFeatures.HasSize
- CoreWebView2WindowFeatures.Height
- CoreWebView2WindowFeatures.Left
- CoreWebView2WindowFeatures.ShouldDisplayMenuBar
- CoreWebView2WindowFeatures.ShouldDisplayScrollBars
- CoreWebView2WindowFeatures.ShouldDisplayStatus
- CoreWebView2WindowFeatures.ShouldDisplayToolbar
- CoreWebView2WindowFeatures.Top
- CoreWebView2WindowFeatures.Width
---

# CoreWebView2WindowFeatures Class



The window features for a WebView popup window.

The fields match the `windowFeatures` passed to `window.open()` as specified in [Window features](https://developer.mozilla.org/docs/Web/API/Window/open#Window_features) on MDN.
There is no requirement for you to respect the values. If your app does not have corresponding UI features (for example, no toolbar) or if all instances of WebView are opened in tabs and do not have distinct size or positions, then your app does not respect the values. You may want to respect values, but perhaps only some apply to the UI of your app. Accordingly, you may respect all, some, or none of the properties as appropriate for your app. For all numeric properties, if the value that is passed to `window.open` is outside the range of an unsigned 32bit int, the resulting value is the absolute value of the maximum for unsigned 32bit integer. If you are not able to parse the value as an integer, it is considered `0`. If the value is a floating point value, it is rounded down to an integer.
In runtime versions 98 or later, the values of `ShouldDisplayMenuBar`, `ShouldDisplayStatus`, `ShouldDisplayToolbar`, and `ShouldDisplayScrollBars` will not directly depend on the equivalent fields in the `windowFeatures` string. Instead, they will all be false if the window is expected to be a popup, and true if it is not.

## Summary

Members|Description
--|--
[HasPosition](#hasposition) | Indicates whether the left and top values are specified.
[HasSize](#hassize) | Indicates whether the height and width values are specified.
[Height](#height) | Gets the height of the window.
[Left](#left) | Specifies the left position of the window.
[ShouldDisplayMenuBar](#shoulddisplaymenubar) | Indicates that the menu bar is displayed.
[ShouldDisplayScrollBars](#shoulddisplayscrollbars) | Indicates that the scroll bars are displayed.
[ShouldDisplayStatus](#shoulddisplaystatus) | Indicates that the status bar is displayed.
[ShouldDisplayToolbar](#shoulddisplaytoolbar) | Indicates that the browser toolbar is displayed.
[Top](#top) | Specifies the top position of the window.
[Width](#width) | Specifies the width of the window.

## Properties

### HasPosition

> readonly  bool HasPosition

Indicates whether the left and top values are specified.

### HasSize

> readonly  bool HasSize

Indicates whether the height and width values are specified.

### Height

> readonly  uint32_t Height

Gets the height of the window.
Ignored if [CoreWebView2WindowFeatures.HasSize](corewebview2windowfeatures.md#hassize) is `false`.

### Left

> readonly  uint32_t Left

Specifies the left position of the window.

Ignored if [CoreWebView2WindowFeatures.HasPosition](corewebview2windowfeatures.md#hasposition) is `false`.

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

Specifies the top position of the window.

Ignored if [CoreWebView2WindowFeatures.HasPosition](corewebview2windowfeatures.md#hasposition) is `false`.

### Width

> readonly  uint32_t Width

Specifies the width of the window.

Ignored if [CoreWebView2WindowFeatures.HasSize](corewebview2windowfeatures.md#hassize) is `false`.






## Referenced by

- [CoreWebView2NewWindowRequestedEventArgs](corewebview2newwindowrequestedeventargs.md)
