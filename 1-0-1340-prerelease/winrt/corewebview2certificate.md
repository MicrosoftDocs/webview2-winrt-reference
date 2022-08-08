---
description: Represents a certificate. Gives access to a certificate's metadata.
title: CoreWebView2Certificate
ms.date: 08/08/2022
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2Certificate
---

# CoreWebView2Certificate Class



Represents a certificate. Gives access to a certificate's metadata.

## Summary

Members|Description
--|--
[DerEncodedSerialNumber](#derencodedserialnumber) | DER encoded serial number of the certificate. Read more about DER at [RFC 7468 DER](https://tools.ietf.org/html/rfc7468#appendix-B).
[DisplayName](#displayname) | Display name for a certificate.
[Issuer](#issuer) | Name of the certificate authority that issued the certificate.
[PemEncodedIssuerCertificateChain](#pemencodedissuercertificatechain) | Returns list of PEM encoded certificate issuer chain. In this list first element is the current certificate followed by intermediate1, intermediate2...intermediateN-1. Root certificate is the last element in the list.
[Subject](#subject) | Subject of the certificate.
[ValidFrom](#validfrom) | The valid start date and time for the certificate as the number of seconds since the UNIX epoch.
[ValidTo](#validto) | The valid expiration date and time for the certificate as the number of seconds since the UNIX epoch.
[ToCertificate](#tocertificate) | Converts this to a [Certificate](/uwp/api/Windows.Security.Cryptography.Certificates.Certificate).
[ToPemEncoding](#topemencoding) | PEM encoded data for the certificate. Returns Base64 encoding of DER encoded certificate. Read more about PEM at [RFC 1421 Privacy Enhanced Mail](https://tools.ietf.org/html/rfc1421).

## Properties

### DerEncodedSerialNumber

> readonly  string DerEncodedSerialNumber

DER encoded serial number of the certificate. Read more about DER at [RFC 7468 DER](https://tools.ietf.org/html/rfc7468#appendix-B).

### DisplayName

> readonly  string DisplayName

Display name for a certificate.

### Issuer

> readonly  string Issuer

Name of the certificate authority that issued the certificate.

### PemEncodedIssuerCertificateChain

> readonly  [`IVectorView`](/uwp/api/Windows.Foundation.Collections.IVectorView-1)&lt;string&gt; PemEncodedIssuerCertificateChain

Returns list of PEM encoded certificate issuer chain. In this list first element is the current certificate followed by intermediate1, intermediate2...intermediateN-1. Root certificate is the last element in the list.

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

- [CoreWebView2ServerCertificateErrorDetectedEventArgs](corewebview2servercertificateerrordetectedeventargs.md)
