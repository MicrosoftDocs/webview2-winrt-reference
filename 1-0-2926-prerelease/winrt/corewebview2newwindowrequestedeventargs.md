---
title: CoreWebView2NewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/01/2024
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2NewWindowRequestedEventArgs
---

# runtimeClass CoreWebView2NewWindowRequestedEventArgs



## Summary

Members|Description
--|--
[Handled](#handled) | 
[IsUserInitiated](#isuserinitiated) | 
[Name](#name) | 
[NewWindow](#newwindow) | 
[OriginalSourceFrameInfo](#originalsourceframeinfo) | 
[Uri](#uri) | 
[WindowFeatures](#windowfeatures) | 
[GetDeferral](#getdeferral) | 

## Properties

### Handled

>  bool Handled

### IsUserInitiated

> readonly  bool IsUserInitiated

### Name

> readonly  string Name

### NewWindow

>  [CoreWebView2](corewebview2.md) NewWindow

### OriginalSourceFrameInfo

> readonly  [CoreWebView2FrameInfo](corewebview2frameinfo.md) OriginalSourceFrameInfo

### Uri

> readonly  string Uri

### WindowFeatures

> readonly  [CoreWebView2WindowFeatures](corewebview2windowfeatures.md) WindowFeatures



## Methods

### GetDeferral

> [Deferral](/uwp/api/Windows.Foundation.Deferral) GetDeferral()






## Referenced by

- [CoreWebView2](corewebview2.md)
