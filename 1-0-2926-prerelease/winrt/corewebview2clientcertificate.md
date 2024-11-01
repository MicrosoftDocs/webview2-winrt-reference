---
title: CoreWebView2ClientCertificate
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/01/2024
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ClientCertificate
---

# runtimeClass CoreWebView2ClientCertificate



## Summary

Members|Description
--|--
[DerEncodedSerialNumber](#derencodedserialnumber) | 
[DisplayName](#displayname) | 
[Issuer](#issuer) | 
[Kind](#kind) | 
[PemEncodedIssuerCertificateChain](#pemencodedissuercertificatechain) | 
[Subject](#subject) | 
[ValidFrom](#validfrom) | 
[ValidTo](#validto) | 
[ToCertificate](#tocertificate) | 
[ToPemEncoding](#topemencoding) | 

## Properties

### DerEncodedSerialNumber

> readonly  string DerEncodedSerialNumber

### DisplayName

> readonly  string DisplayName

### Issuer

> readonly  string Issuer

### Kind

> readonly  [CoreWebView2ClientCertificateKind](corewebview2clientcertificatekind.md) Kind

### PemEncodedIssuerCertificateChain

> readonly  [`IVectorView`](/uwp/api/Windows.Foundation.Collections.IVectorView-1)&lt;string&gt; PemEncodedIssuerCertificateChain

### Subject

> readonly  string Subject

### ValidFrom

> readonly  double ValidFrom

### ValidTo

> readonly  double ValidTo



## Methods

### ToCertificate

> [Certificate](/uwp/api/Windows.Security.Cryptography.Certificates.Certificate) ToCertificate()



### ToPemEncoding

> string ToPemEncoding()






## Referenced by

- [CoreWebView2ClientCertificateRequestedEventArgs](corewebview2clientcertificaterequestedeventargs.md)
