---
description: 
title: CoreWebView2ServerCertificateErrorDetectedEventArgs
ms.date: 11/15/2024
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ServerCertificateErrorDetectedEventArgs
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2ServerCertificateErrorDetectedEventArgs
- CoreWebView2ServerCertificateErrorDetectedEventArgs.Action
- CoreWebView2ServerCertificateErrorDetectedEventArgs.ErrorStatus
- CoreWebView2ServerCertificateErrorDetectedEventArgs.RequestUri
- CoreWebView2ServerCertificateErrorDetectedEventArgs.ServerCertificate
- CoreWebView2ServerCertificateErrorDetectedEventArgs.GetDeferral
---

# CoreWebView2ServerCertificateErrorDetectedEventArgs Class



## Summary

Members|Description
--|--
[Action](#action) | 
[ErrorStatus](#errorstatus) | 
[RequestUri](#requesturi) | 
[ServerCertificate](#servercertificate) | 
[GetDeferral](#getdeferral) | 

## Properties

### Action

>  [CoreWebView2ServerCertificateErrorAction](corewebview2servercertificateerroraction.md) Action

### ErrorStatus

> readonly  [CoreWebView2WebErrorStatus](corewebview2weberrorstatus.md) ErrorStatus

### RequestUri

> readonly  string RequestUri

### ServerCertificate

> readonly  [CoreWebView2Certificate](corewebview2certificate.md) ServerCertificate



## Methods

### GetDeferral

> [Deferral](/uwp/api/Windows.Foundation.Deferral) GetDeferral()






## Referenced by

- [CoreWebView2](corewebview2.md)
