---
description: Web Texture that receives from the Javascript.
title: CoreWebView2WebTexture
ms.date: 11/06/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2WebTexture
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- Microsoft.Web.WebView2.Core.CoreWebView2WebTexture
- Microsoft.Web.WebView2.Core.CoreWebView2WebTexture.Resource
- Microsoft.Web.WebView2.Core.CoreWebView2WebTexture.Timestamp
- Microsoft.Web.WebView2.Core.CoreWebView2WebTexture.get_Resource
- Microsoft.Web.WebView2.Core.CoreWebView2WebTexture.get_Timestamp
---

# CoreWebView2WebTexture Class



Web Texture that receives from the Javascript.

## Summary

Members|Description
--|--
[Resource](#resource) | D2D texture resource that the host can read from.
[Timestamp](#timestamp) | Presented texture timestamp from the Javascript.

## Properties

### Resource

> readonly  Object Resource

D2D texture resource that the host can read from.

### Timestamp

> readonly  uint64_t Timestamp

Presented texture timestamp from the Javascript.







## Referenced by

- [CoreWebView2TextureStreamWebTextureReceivedEventArgs](corewebview2texturestreamwebtexturereceivedeventargs.md)
