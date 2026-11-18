---
description: Web Texture that receives from the Javascript.
title: CoreWebView2WebTexture
ms.date: 11/11/2026
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2WebTexture
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2WebTexture
- CoreWebView2WebTexture.Resource
- CoreWebView2WebTexture.Timestamp
---

# CoreWebView2WebTexture Class



Web Texture that receives from the Javascript.

## Summary

Members|Description
--|--
[Resource](#resource) | D2D texture resource that the host can read from.
[Timestamp](#timestamp) | The timestamp of the web texture.

## Properties

### Resource

> readonly  Object Resource

D2D texture resource that the host can read from.

### Timestamp

> readonly  uint64_t Timestamp

The timestamp of the web texture.
Javascript can set this value with any value, but it is suggested to use same value of its original video frame that is a value of PresentTexture so that the host is able to tell the receiving texture delta.






## Referenced by

- [CoreWebView2TextureStreamWebTextureReceivedEventArgs](corewebview2texturestreamwebtexturereceivedeventargs.md)
