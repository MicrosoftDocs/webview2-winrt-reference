---
description: Represents a client certificate. Gives access to a certificate's metadata.
title: CoreWebView2ClientCertificate
ms.date: 09/18/2023
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



Represents a client certificate. Gives access to a certificate's metadata.

## Summary

Members|Description
--|--
[DerEncodedSerialNumber](#derencodedserialnumber) | Base64 encoding of DER encoded serial number of the certificate. Read more about DER at [RFC 7468 DER](https://tools.ietf.org/html/rfc7468#appendix-B).
[DisplayName](#displayname) | Display name for a certificate.
[Issuer](#issuer) | Name of the certificate authority that issued the certificate.
[Kind](#kind) | Kind of a certificate. See [CoreWebView2ClientCertificateKind](corewebview2clientcertificatekind.md) for descriptions.
[PemEncodedIssuerCertificateChain](#pemencodedissuercertificatechain) | Returns list of PEM encoded client certificate issuer chain. In this list first element is the current certificate followed by intermediate1, intermediate2...intermediateN-1. Root certificate is the last element in the list.
[Subject](#subject) | Subject of the certificate.
[ValidFrom](#validfrom) | The valid start date and time for the certificate as the number of seconds since the UNIX epoch.
[ValidTo](#validto) | The valid expiration date and time for the certificate as the number of seconds since the UNIX epoch.
[ToCertificate](#tocertificate) | Converts this to a [Certificate](/uwp/api/Windows.Security.Cryptography.Certificates.Certificate).
[ToPemEncoding](#topemencoding) | PEM encoded data for the certificate. Returns Base64 encoding of DER encoded certificate. Read more about PEM at [RFC 1421 Privacy Enhanced Mail](https://tools.ietf.org/html/rfc1421).

## Properties

### DerEncodedSerialNumber

> readonly  string DerEncodedSerialNumber

Base64 encoding of DER encoded serial number of the certificate. Read more about DER at [RFC 7468 DER](https://tools.ietf.org/html/rfc7468#appendix-B).

### DisplayName

> readonly  string DisplayName

Display name for a certificate.

### Issuer

> readonly  string Issuer

Name of the certificate authority that issued the certificate.

### Kind

> readonly  [CoreWebView2ClientCertificateKind](corewebview2clientcertificatekind.md) Kind

Kind of a certificate. See [CoreWebView2ClientCertificateKind](corewebview2clientcertificatekind.md) for descriptions.

### PemEncodedIssuerCertificateChain

> readonly  [`IVectorView`](/uwp/api/Windows.Foundation.Collections.IVectorView-1)&lt;string&gt; PemEncodedIssuerCertificateChain

Returns list of PEM encoded client certificate issuer chain. In this list first element is the current certificate followed by intermediate1, intermediate2...intermediateN-1. Root certificate is the last element in the list.

### Subject

> readonly  string Subject

Subject of the certificate.

### ValidFrom

> readonly  double ValidFrom

The valid start date and time for the certificate as the number of seconds since the UNIX epoch.

### ValidTo

> readonly  double ValidTo

The valid expiration date and time for the certificate as the number of seconds since the UNIX epoch.



## Methods

### ToCertificate

> [Certificate](/uwp/api/Windows.Security.Cryptography.Certificates.Certificate) ToCertificate()

Converts this to a [Certificate](/uwp/api/Windows.Security.Cryptography.Certificates.Certificate).



### ToPemEncoding

> string ToPemEncoding()

PEM encoded data for the certificate. Returns Base64 encoding of DER encoded certificate. Read more about PEM at [RFC 1421 Privacy Enhanced Mail](https://tools.ietf.org/html/rfc1421).






## Referenced by

- [CoreWebView2ClientCertificateRequestedEventArgs](corewebview2clientcertificaterequestedeventargs.md)
