---
description: 
title: CoreWebView2ClientCertificate
ms.date: 10/16/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ClientCertificate
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- Microsoft.Web.WebView2.Core.CoreWebView2ClientCertificate
- Microsoft.Web.WebView2.Core.CoreWebView2ClientCertificate.DerEncodedSerialNumber
- Microsoft.Web.WebView2.Core.CoreWebView2ClientCertificate.DisplayName
- Microsoft.Web.WebView2.Core.CoreWebView2ClientCertificate.Issuer
- Microsoft.Web.WebView2.Core.CoreWebView2ClientCertificate.Kind
- Microsoft.Web.WebView2.Core.CoreWebView2ClientCertificate.PemEncodedIssuerCertificateChain
- Microsoft.Web.WebView2.Core.CoreWebView2ClientCertificate.Subject
- Microsoft.Web.WebView2.Core.CoreWebView2ClientCertificate.ValidFrom
- Microsoft.Web.WebView2.Core.CoreWebView2ClientCertificate.ValidTo
- Microsoft.Web.WebView2.Core.CoreWebView2ClientCertificate.ToCertificate
- Microsoft.Web.WebView2.Core.CoreWebView2ClientCertificate.ToPemEncoding
- Microsoft.Web.WebView2.Core.CoreWebView2ClientCertificate.get_DerEncodedSerialNumber
- Microsoft.Web.WebView2.Core.CoreWebView2ClientCertificate.get_DisplayName
- Microsoft.Web.WebView2.Core.CoreWebView2ClientCertificate.get_Issuer
- Microsoft.Web.WebView2.Core.CoreWebView2ClientCertificate.get_Kind
- Microsoft.Web.WebView2.Core.CoreWebView2ClientCertificate.get_PemEncodedIssuerCertificateChain
- Microsoft.Web.WebView2.Core.CoreWebView2ClientCertificate.get_Subject
- Microsoft.Web.WebView2.Core.CoreWebView2ClientCertificate.get_ValidFrom
- Microsoft.Web.WebView2.Core.CoreWebView2ClientCertificate.get_ValidTo
---

# CoreWebView2ClientCertificate Class



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
