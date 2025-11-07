---
description: Event args for the BasicAuthenticationRequested event. Will contain the request that led to the HTTP authorization challenge, the challenge and allows the host to provide authentication response or cancel the request.
title: CoreWebView2BasicAuthenticationRequestedEventArgs
ms.date: 11/03/2025
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2BasicAuthenticationRequestedEventArgs
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2BasicAuthenticationRequestedEventArgs
- CoreWebView2BasicAuthenticationRequestedEventArgs.Cancel
- CoreWebView2BasicAuthenticationRequestedEventArgs.Challenge
- CoreWebView2BasicAuthenticationRequestedEventArgs.Response
- CoreWebView2BasicAuthenticationRequestedEventArgs.Uri
- CoreWebView2BasicAuthenticationRequestedEventArgs.GetDeferral
---

# CoreWebView2BasicAuthenticationRequestedEventArgs Class



Event args for the BasicAuthenticationRequested event. Will contain the request that led to the HTTP authorization challenge, the challenge and allows the host to provide authentication response or cancel the request.

## Summary

Members|Description
--|--
[Cancel](#cancel) | Indicates whether to cancel the authentication request.
[Challenge](#challenge) | The authentication challenge string.
[Response](#response) | Response to the authentication request with credentials.
[Uri](#uri) | The URI that led to the authentication challenge. For proxy authentication requests, this will be the URI of the proxy server.
[GetDeferral](#getdeferral) | Gets a Deferral object.

## Properties

### Cancel

>  bool Cancel

Indicates whether to cancel the authentication request.
`false` by default. If set to `true`, Response will be ignored.

### Challenge

> readonly  string Challenge

The authentication challenge string.

### Response

> readonly  [CoreWebView2BasicAuthenticationResponse](corewebview2basicauthenticationresponse.md) Response

Response to the authentication request with credentials.
This object will be populated by the app if the host would like to provide authentication credentials.

### Uri

> readonly  string Uri

The URI that led to the authentication challenge. For proxy authentication requests, this will be the URI of the proxy server.



## Methods

### GetDeferral

> [Deferral](/uwp/api/Windows.Foundation.Deferral) GetDeferral()

Gets a Deferral object.
Use this Deferral to defer the decision to show the Basic Authentication dialog.






## Referenced by

- [CoreWebView2](corewebview2.md)
