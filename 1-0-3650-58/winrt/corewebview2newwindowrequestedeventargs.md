---
description: Event args for the CoreWebView2.NewWindowRequested event.
title: CoreWebView2NewWindowRequestedEventArgs
ms.date: 12/02/2025
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2NewWindowRequestedEventArgs
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2NewWindowRequestedEventArgs
- CoreWebView2NewWindowRequestedEventArgs.Handled
- CoreWebView2NewWindowRequestedEventArgs.IsUserInitiated
- CoreWebView2NewWindowRequestedEventArgs.Name
- CoreWebView2NewWindowRequestedEventArgs.NewWindow
- CoreWebView2NewWindowRequestedEventArgs.OriginalSourceFrameInfo
- CoreWebView2NewWindowRequestedEventArgs.Uri
- CoreWebView2NewWindowRequestedEventArgs.WindowFeatures
- CoreWebView2NewWindowRequestedEventArgs.GetDeferral
---

# CoreWebView2NewWindowRequestedEventArgs Class



Event args for the [CoreWebView2.NewWindowRequested](corewebview2.md#newwindowrequested) event.

## Summary

Members|Description
--|--
[Handled](#handled) | Indicates whether the [CoreWebView2.NewWindowRequested](corewebview2.md#newwindowrequested) event is handled by host.
[IsUserInitiated](#isuserinitiated) | `true` when the new window request was initiated through a user gesture such as selecting an anchor tag with target.
[Name](#name) | Gets the name of the new window.
[NewWindow](#newwindow) | Gets the new window or sets a WebView as a result of the new window requested.
[OriginalSourceFrameInfo](#originalsourceframeinfo) | The frame info of the frame where the new window request originated.
[Uri](#uri) | Gets the target uri of the new window request.
[WindowFeatures](#windowfeatures) | Gets the window features specified by the `window.open()` call. These features should be considered for positioning and sizing of new WebView windows.
[GetDeferral](#getdeferral) | Gets a Deferral object and put the event into a deferred state.

## Properties

### Handled

>  bool Handled

Indicates whether the [CoreWebView2.NewWindowRequested](corewebview2.md#newwindowrequested) event is handled by host.
If this is `false` and no [CoreWebView2NewWindowRequestedEventArgs.NewWindow](corewebview2newwindowrequestedeventargs.md#newwindow) is set, the WebView opens a popup window and returns the opened `WindowProxy` to the opener script. Note that in this case, there is no avenue to control the popup window from the app. If set to `true` and no [CoreWebView2NewWindowRequestedEventArgs.NewWindow](corewebview2newwindowrequestedeventargs.md#newwindow) is set for `window.open()`, the opened `proxy` is for a dummy window object, but this window does not load and is immediately closed. The default value is `false`.

### IsUserInitiated

> readonly  bool IsUserInitiated

`true` when the new window request was initiated through a user gesture such as selecting an anchor tag with target.
The Microsoft Edge popup blocker is disabled for WebView so the app is able to use this flag to block non-user initiated popups.

### Name

> readonly  string Name

Gets the name of the new window.
This window can be created via `window.open(url, windowName)`, where the windowName parameter corresponds to `Name` property.
If no windowName is passed to `window.open`, then the `Name` property will be set to an empty string. Additionally, if window is opened through other means, such as `<a target="windowName">` or `<iframe name="windowName">`, then the `Name` property will be set accordingly. In the case of target=_blank, the `Name` property will be an empty string.
Opening a window via Ctrl+clicking a link would result in the `Name` property being set to an empty string.

### NewWindow

>  [CoreWebView2](corewebview2.md) NewWindow

Gets the new window or sets a WebView as a result of the new window requested.
Provides a WebView as the target for a `window.open()` from inside the requesting WebView. If this is set, the top-level window of this WebView is returned as the opened [WindowProxy](https://developer.mozilla.org/docs/glossary/windowproxy) to the opener script. If this is not set, then [CoreWebView2NewWindowRequestedEventArgs.Handled](corewebview2newwindowrequestedeventargs.md#handled) is checked to determine behavior for the [CoreWebView2.NewWindowRequested](corewebview2.md#newwindowrequested).
The methods which should affect the new web contents like [CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync](corewebview2.md#addscripttoexecuteondocumentcreatedasync) has to be called and completed before setting NewWindow. Other methods which should affect the new web contents like [CoreWebView2.WebResourceRequested](corewebview2.md#webresourcerequested) have to be called after setting NewWindow. It is best not to use [CoreWebView2.RemoveScriptToExecuteOnDocumentCreated](corewebview2.md#removescripttoexecuteondocumentcreated) before setting NewWindow, otherwise it may not work for later added scripts.
WebView provided in the `NewWindow` property must be on the same [CoreWebView2Environment](corewebview2environment.md) as the opener WebView and cannot be navigated. Changes to settings should be made before setting NewWindow to ensure that those settings take effect for the newly setup WebView. The new WebView must have the same profile as the opener WebView.

### OriginalSourceFrameInfo

> readonly  [CoreWebView2FrameInfo](corewebview2frameinfo.md) OriginalSourceFrameInfo

The frame info of the frame where the new window request originated.
The `OriginalSourceFrameInfo` is a snapshot of frame information at the time when the new window was requested. See [CoreWebView2FrameInfo](corewebview2frameinfo.md) for details on frame properties.

### Uri

> readonly  string Uri

Gets the target uri of the new window request.

### WindowFeatures

> readonly  [CoreWebView2WindowFeatures](corewebview2windowfeatures.md) WindowFeatures

Gets the window features specified by the `window.open()` call. These features should be considered for positioning and sizing of new WebView windows.



## Methods

### GetDeferral

> [Deferral](/uwp/api/Windows.Foundation.Deferral) GetDeferral()

Gets a Deferral object and put the event into a deferred state.
Use this to Complete the window open request at a later time. While this event is deferred the opener window returns a WindowProxy to an un-navigated window, which navigates when the deferral is complete.






## Referenced by

- [CoreWebView2](corewebview2.md)
