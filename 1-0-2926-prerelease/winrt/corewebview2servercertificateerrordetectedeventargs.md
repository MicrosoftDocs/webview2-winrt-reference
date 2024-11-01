---
title: CoreWebView2ServerCertificateErrorDetectedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/01/2024
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ServerCertificateErrorDetectedEventArgs
---

# runtimeClass CoreWebView2ServerCertificateErrorDetectedEventArgs



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
