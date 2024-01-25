---
description: Specifies the action type when server certificate error is detected to be used in the CoreWebView2ServerCertificateErrorDetectedEventArgs.
title: CoreWebView2ServerCertificateErrorAction
ms.date: 01/29/2024
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ServerCertificateErrorAction
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- Microsoft.Web.WebView2.Core.CoreWebView2ServerCertificateErrorAction
---

# CoreWebView2ServerCertificateErrorAction Enum

Specifies the action type when server certificate error is detected to be used in the [CoreWebView2ServerCertificateErrorDetectedEventArgs](corewebview2servercertificateerrordetectedeventargs.md).

| Name |  Value | Description |
|--|--|--|
|`AlwaysAllow` | 0x0  |  Indicates to ignore the warning and continue the request with the TLS certificate. This decision is cached for the RequestUri's host and the server certificate in the session.|
|`Cancel` | 0x1  |  Indicates to reject the certificate and cancel the request.|
|`Default` | 0x2  |  Indicates to display the default TLS interstitial error page to user for page navigations. For others TLS certificate is rejected and the request is cancelled.|


## Referenced by

- [CoreWebView2ServerCertificateErrorDetectedEventArgs](corewebview2servercertificateerrordetectedeventargs.md)
