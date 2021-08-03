---
description: Interop interface for the CoreWebView2Environment WinRT object to allow WinRT end developers to be able to use COM interfaces as parameters for some methods.
title: WebView2 WinRT COM ICoreWebView2EnvironmentInterop
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/11/2021
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, winrt, interop, edge, ICoreWebView2, ICoreWebView2Controller, browser control, edge html, ICoreWebView2EnvironmentInterop
---

# interface ICoreWebView2EnvironmentInterop

```
interface ICoreWebView2EnvironmentInterop
  : public IUnknown
```

Interop interface for the CoreWebView2Environment WinRT object to allow WinRT end developers to be able to use COM interfaces as parameters for some methods.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
[GetProviderForHwnd](#getproviderforhwnd) | Returns the UI Automation Provider for the ICoreWebView2CompositionController that corresponds with the given HWND.

## Members

#### GetProviderForHwnd

Returns the UI Automation Provider for the ICoreWebView2CompositionController that corresponds with the given HWND.

> public HRESULT [GetProviderForHwnd](#getproviderforhwnd)(HWND hwnd,IUnknown ** provider)

