---
description: 
title: CoreWebView2Certificate
ms.date: 10/16/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2Certificate
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- Microsoft.Web.WebView2.Core.CoreWebView2Certificate
- Microsoft.Web.WebView2.Core.CoreWebView2Certificate.DerEncodedSerialNumber
- Microsoft.Web.WebView2.Core.CoreWebView2Certificate.DisplayName
- Microsoft.Web.WebView2.Core.CoreWebView2Certificate.Issuer
- Microsoft.Web.WebView2.Core.CoreWebView2Certificate.PemEncodedIssuerCertificateChain
- Microsoft.Web.WebView2.Core.CoreWebView2Certificate.Subject
- Microsoft.Web.WebView2.Core.CoreWebView2Certificate.ValidFrom
- Microsoft.Web.WebView2.Core.CoreWebView2Certificate.ValidTo
- Microsoft.Web.WebView2.Core.CoreWebView2Certificate.ToCertificate
- Microsoft.Web.WebView2.Core.CoreWebView2Certificate.ToPemEncoding
- Microsoft.Web.WebView2.Core.CoreWebView2Certificate.get_DerEncodedSerialNumber
- Microsoft.Web.WebView2.Core.CoreWebView2Certificate.get_DisplayName
- Microsoft.Web.WebView2.Core.CoreWebView2Certificate.get_Issuer
- Microsoft.Web.WebView2.Core.CoreWebView2Certificate.get_PemEncodedIssuerCertificateChain
- Microsoft.Web.WebView2.Core.CoreWebView2Certificate.get_Subject
- Microsoft.Web.WebView2.Core.CoreWebView2Certificate.get_ValidFrom
- Microsoft.Web.WebView2.Core.CoreWebView2Certificate.get_ValidTo
---

# CoreWebView2Certificate Class



## Summary

Members|Description
--|--
[DerEncodedSerialNumber](#derencodedserialnumber) | 
[DisplayName](#displayname) | 
[Issuer](#issuer) | 
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

- [CoreWebView2ServerCertificateErrorDetectedEventArgs](corewebview2servercertificateerrordetectedeventargs.md)
