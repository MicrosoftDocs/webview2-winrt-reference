---
description: Interop interface for the CoreWebView2 WinRT object to allow WinRT end developers to be able to use COM interfaces as parameters for some methods.
title: WebView2 WinRT COM ICoreWebView2Interop2
ms.date: 06/19/2024
keywords: IWebView2, IWebView2WebView, webview2, webview, winrt, interop, edge, ICoreWebView2, ICoreWebView2Controller, browser control, edge html, ICoreWebView2Interop
topic_type: 
- APIRef
api_name:
- ICoreWebView2Interop2
- ICoreWebView2Interop2.GetComICoreWebView2
api_type:
- COM
api_location:
- embeddedbrowserwebview.dll
---

# interface ICoreWebView2Interop2

```
interface ICoreWebView2Interop2
  : public IUnknown
```

Interop interface for the CoreWebView2 WinRT object to allow WinRT end developers to be able to use COM interfaces as parameters for some methods.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
[GetComICoreWebView2](#getcomicorewebview2) | Get a COM ICoreWebView2 interface corresponding to this WinRT CoreWebView2 object.

This interface is implemented by the Microsoft.Web.WebView2.Core.CoreWebView2 runtime class.

## Members

#### GetComICoreWebView2

Get a COM ICoreWebView2 interface corresponding to this WinRT CoreWebView2 object.

> public HRESULT [GetComICoreWebView2](#getcomicorewebview2)(ICoreWebView2 ** coreWebView2)

