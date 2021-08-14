---
title: CoreWebView2ControllerWindowReference
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/14/2021
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ControllerWindowReference
---

# runtimeClass CoreWebView2ControllerWindowReference



References an HWND or a CoreWindow.
This is used in [CoreWebView2Controller](corewebview2controller.md) APIs that take a window in order to support either an HWND or a CoreWindow parameter.

## Summary

Members|Description
--|--
[CoreWindow](#corewindow) | The CoreWindow object of this window reference.
[WindowHandle](#windowhandle) | The HWND window handle of this window reference.
[CreateFromCoreWindow](#createfromcorewindow) | Create a CoreWebView2ControllerWindowReference from a CoreWindow.
[CreateFromWindowHandle](#createfromwindowhandle) | Create a CoreWebView2ControllerWindowReference from an HWND.

## Properties

### CoreWindow

> readonly  [CoreWindow](/uwp/api/Windows.UI.Core.CoreWindow) CoreWindow

The CoreWindow object of this window reference.
This may be null. When this is non-null, the [WindowHandle](#windowhandle) property is the HWND for this CoreWindow.

### WindowHandle

> readonly  uint64_t WindowHandle

The HWND window handle of this window reference.



## Methods

### CreateFromCoreWindow

> static [CoreWebView2ControllerWindowReference](corewebview2controllerwindowreference.md) CreateFromCoreWindow([CoreWindow](/uwp/api/Windows.UI.Core.CoreWindow) coreWindow)

Create a CoreWebView2ControllerWindowReference from a CoreWindow.
The resulting CoreWebView2ControllerWindowReference will have its [CoreWindow](#corewindow) property set to the coreWindow parameter value and a [WindowHandle](#windowhandle) property set to the HWND of that coreWindow.



### CreateFromWindowHandle

> static [CoreWebView2ControllerWindowReference](corewebview2controllerwindowreference.md) CreateFromWindowHandle(uint64_t windowHandle)

Create a CoreWebView2ControllerWindowReference from an HWND.
The resulting CoreWebView2ControllerWindowReference will have its [WindowHandle](#windowhandle) property set to the windowHandle parameter value and a null [CoreWindow](#corewindow) property.






## Referenced by

- [CoreWebView2CompositionController](corewebview2compositioncontroller.md)
- [CoreWebView2Controller](corewebview2controller.md)
- [CoreWebView2Environment](corewebview2environment.md)
