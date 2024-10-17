---
description: Interop interface for the CoreWebView2 WinRT object to allow WinRT end developers to be able to use COM interfaces as parameters for some methods.
title: WebView2 WinRT COM ICoreWebView2Interop
ms.date: 10/21/2024
keywords: IWebView2, IWebView2WebView, webview2, webview, winrt, interop, edge, ICoreWebView2, ICoreWebView2Controller, browser control, edge html, ICoreWebView2Interop
topic_type: 
- APIRef
api_name:
- ICoreWebView2Interop
- ICoreWebView2Interop.AddHostObjectToScript
api_type:
- COM
api_location:
- embeddedbrowserwebview.dll
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

This interface is implemented by the Microsoft.Web.WebView2.Core.CoreWebView2 runtime class.

## Members

#### AddHostObjectToScript

Add the provided host object to script running in the WebView with the specified name.

> public HRESULT [AddHostObjectToScript](#addhostobjecttoscript)(LPCWSTR name, VARIANT * object)

See the documentation for ICoreWebView2::AddHostObjectToScript for more information.

