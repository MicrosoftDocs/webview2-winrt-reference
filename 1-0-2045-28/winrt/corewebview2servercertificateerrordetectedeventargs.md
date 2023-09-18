---
description: Event args for the CoreWebView2.ServerCertificateErrorDetected event.
title: CoreWebView2ServerCertificateErrorDetectedEventArgs
ms.date: 09/18/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ServerCertificateErrorDetectedEventArgs
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- Microsoft.Web.WebView2.Core.CoreWebView2ServerCertificateErrorDetectedEventArgs
- Microsoft.Web.WebView2.Core.CoreWebView2ServerCertificateErrorDetectedEventArgs.Action
- Microsoft.Web.WebView2.Core.CoreWebView2ServerCertificateErrorDetectedEventArgs.ErrorStatus
- Microsoft.Web.WebView2.Core.CoreWebView2ServerCertificateErrorDetectedEventArgs.RequestUri
- Microsoft.Web.WebView2.Core.CoreWebView2ServerCertificateErrorDetectedEventArgs.ServerCertificate
- Microsoft.Web.WebView2.Core.CoreWebView2ServerCertificateErrorDetectedEventArgs.GetDeferral
- Microsoft.Web.WebView2.Core.CoreWebView2ServerCertificateErrorDetectedEventArgs.get_Action
- Microsoft.Web.WebView2.Core.CoreWebView2ServerCertificateErrorDetectedEventArgs.get_ErrorStatus
- Microsoft.Web.WebView2.Core.CoreWebView2ServerCertificateErrorDetectedEventArgs.get_RequestUri
- Microsoft.Web.WebView2.Core.CoreWebView2ServerCertificateErrorDetectedEventArgs.get_ServerCertificate
- Microsoft.Web.WebView2.Core.CoreWebView2ServerCertificateErrorDetectedEventArgs.put_Action
---

# CoreWebView2ServerCertificateErrorDetectedEventArgs Class



Event args for the [CoreWebView2.ServerCertificateErrorDetected](corewebview2.md#servercertificateerrordetected) event.

## Summary

Members|Description
--|--
[Action](#action) | The action of the server certificate error detection.
[ErrorStatus](#errorstatus) | The TLS error code for the invalid certificate.
[RequestUri](#requesturi) | URI associated with the request for the invalid certificate.
[ServerCertificate](#servercertificate) | Returns the [CoreWebView2Certificate](corewebview2certificate.md).
[GetDeferral](#getdeferral) | Gets a Deferral object.

## Properties

### Action

>  [CoreWebView2ServerCertificateErrorAction](corewebview2servercertificateerroraction.md) Action

The action of the server certificate error detection.
The default value is [CoreWebView2ServerCertificateErrorAction](corewebview2servercertificateerroraction.md).Default.

### ErrorStatus

> readonly  [CoreWebView2WebErrorStatus](corewebview2weberrorstatus.md) ErrorStatus

The TLS error code for the invalid certificate.

### RequestUri

> readonly  string RequestUri

URI associated with the request for the invalid certificate.

### ServerCertificate

> readonly  [CoreWebView2Certificate](corewebview2certificate.md) ServerCertificate

Returns the [CoreWebView2Certificate](corewebview2certificate.md).



## Methods

### GetDeferral

> [Deferral](/uwp/api/Windows.Foundation.Deferral) GetDeferral()

Gets a Deferral object.
Use this to Complete the event at a later time.






## Referenced by

- [CoreWebView2](corewebview2.md)