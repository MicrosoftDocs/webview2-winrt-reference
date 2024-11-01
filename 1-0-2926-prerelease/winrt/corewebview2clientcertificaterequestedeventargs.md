---
title: CoreWebView2ClientCertificateRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/01/2024
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ClientCertificateRequestedEventArgs
---

# runtimeClass CoreWebView2ClientCertificateRequestedEventArgs



## Summary

Members|Description
--|--
[AllowedCertificateAuthorities](#allowedcertificateauthorities) | 
[Cancel](#cancel) | 
[Handled](#handled) | 
[Host](#host) | 
[IsProxy](#isproxy) | 
[MutuallyTrustedCertificates](#mutuallytrustedcertificates) | 
[Port](#port) | 
[SelectedCertificate](#selectedcertificate) | 
[GetDeferral](#getdeferral) | 

## Properties

### AllowedCertificateAuthorities

> readonly  [`IVectorView`](/uwp/api/Windows.Foundation.Collections.IVectorView-1)&lt;string&gt; AllowedCertificateAuthorities

### Cancel

>  bool Cancel

### Handled

>  bool Handled

### Host

> readonly  string Host

### IsProxy

> readonly  bool IsProxy

### MutuallyTrustedCertificates

> readonly  [`IVectorView`](/uwp/api/Windows.Foundation.Collections.IVectorView-1)&lt;[CoreWebView2ClientCertificate](corewebview2clientcertificate.md)&gt; MutuallyTrustedCertificates

### Port

> readonly  int Port

### SelectedCertificate

>  [CoreWebView2ClientCertificate](corewebview2clientcertificate.md) SelectedCertificate



## Methods

### GetDeferral

> [Deferral](/uwp/api/Windows.Foundation.Deferral) GetDeferral()






## Referenced by

- [CoreWebView2](corewebview2.md)
