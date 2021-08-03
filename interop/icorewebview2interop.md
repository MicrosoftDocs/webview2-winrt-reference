---
description: Interop interface for the CoreWebView2 WinRT object to allow WinRT end developers to be able to use COM interfaces as parameters for some methods.
title: WebView2 WinRT COM ICoreWebView2Interop
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/11/2021
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, winrt, interop, edge, ICoreWebView2, ICoreWebView2Controller, browser control, edge html, ICoreWebView2Interop
---

# interface ICoreWebView2Interop

```
interface ICoreWebView2Interop
  : public IUnknown
```

Interop interface for the CoreWebView2 WinRT object to allow WinRT end developers to be able to use COM interfaces as parameters for some methods.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
[AddHostObjectToScript](#addhostobjecttoscript) | Add the provided host object to script running in the WebView with the specified name.

## Members

#### AddHostObjectToScript

Add the provided host object to script running in the WebView with the specified name.

> public HRESULT [AddHostObjectToScript](#addhostobjecttoscript)(LPCWSTR name,VARIANT * object)

See the documentation for ICoreWebView2::AddHostObjectToScript for more information.

