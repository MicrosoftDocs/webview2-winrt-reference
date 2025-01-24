---
description: Interop interface for the CoreWebView2Environment WinRT object to allow WinRT end developers to be able to use COM interfaces as parameters for some methods.
title: WebView2 WinRT COM ICoreWebView2EnvironmentInterop
ms.date: 01/16/2025
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
[GetAutomationProviderForWindow](#getautomationproviderforwindow) | Returns the UI Automation Provider for the ICoreWebView2CompositionController that corresponds with the given HWND.

This interface is implemented by the Microsoft.Web.WebView2.Core.CoreWebView2Environment runtime class.

## Applies to

Product                         | Introduced
--------------------------------|---------------------------------------------
WebView2 WinRT            |    1.0.992.28
WebView2 WinRT Prerelease |    1.0.955

## Members

#### GetAutomationProviderForWindow

Returns the UI Automation Provider for the ICoreWebView2CompositionController that corresponds with the given HWND.

> public HRESULT [GetAutomationProviderForWindow](#getautomationproviderforwindow)(HWND hwnd, IUnknown ** provider)

See the documentation for ICoreWebView2Environment::GetAutomationProviderForWindow for more information.

