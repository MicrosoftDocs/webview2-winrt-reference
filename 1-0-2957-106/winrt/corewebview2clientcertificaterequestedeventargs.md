---
title: CoreWebView2ClientCertificateRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/13/2025
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ClientCertificateRequestedEventArgs
---

# runtimeClass CoreWebView2ClientCertificateRequestedEventArgs



Event args for the [CoreWebView2.ClientCertificateRequested](corewebview2.md#clientcertificaterequested) event.

## Summary

Members|Description
--|--
[AllowedCertificateAuthorities](#allowedcertificateauthorities) | The list contains Base64 encoding of DER encoded distinguished names of certificate authorities allowed by the server.
[Cancel](#cancel) | Indicates whether to cancel the certificate selection.
[Handled](#handled) | Indicates whether the event has been handled by host.
[Host](#host) | Returns host name of the server that requested client certificate authentication.
[IsProxy](#isproxy) | Returns true if the server that issued this request is an http proxy. Returns false if the server is the origin server.
[MutuallyTrustedCertificates](#mutuallytrustedcertificates) | Returns the list of [CoreWebView2ClientCertificate](corewebview2clientcertificate.md) when client certificate authentication is requested. The list contains mutually trusted CA certificate.
[Port](#port) | Returns port of the server that requested client certificate authentication.
[SelectedCertificate](#selectedcertificate) | Selected certificate to respond to the server.
[GetDeferral](#getdeferral) | Gets a Deferral object.

## Properties

### AllowedCertificateAuthorities

> readonly  [`IVectorView`](/uwp/api/Windows.Foundation.Collections.IVectorView-1)&lt;string&gt; AllowedCertificateAuthorities

The list contains Base64 encoding of DER encoded distinguished names of certificate authorities allowed by the server.

### Cancel

>  bool Cancel

Indicates whether to cancel the certificate selection.
If canceled, the request is aborted regardless of the [CoreWebView2ClientCertificateRequestedEventArgs.Handled](corewebview2clientcertificaterequestedeventargs.md#handled) property. By default the value is false.

### Handled

>  bool Handled

Indicates whether the event has been handled by host.
Set to true to respond to the server with or without a certificate. If this flag is true with a [CoreWebView2ClientCertificateRequestedEventArgs.SelectedCertificate](corewebview2clientcertificaterequestedeventargs.md#selectedcertificate) it responds to the server with the selected certificate otherwise respond to the server without a certificate. By default the value of [CoreWebView2ClientCertificateRequestedEventArgs.Handled](corewebview2clientcertificaterequestedeventargs.md#handled) and [CoreWebView2ClientCertificateRequestedEventArgs.Cancel](corewebview2clientcertificaterequestedeventargs.md#cancel) are false and display default client certificate selection dialog prompt to allow the user to choose a certificate. The [CoreWebView2ClientCertificateRequestedEventArgs.SelectedCertificate](corewebview2clientcertificaterequestedeventargs.md#selectedcertificate) is ignored unless [CoreWebView2ClientCertificateRequestedEventArgs.Handled](corewebview2clientcertificaterequestedeventargs.md#handled) is set to true.

### Host

> readonly  string Host

Returns host name of the server that requested client certificate authentication.
Normalization rules applied to the hostname are:

- Convert to lowercase characters for ascii characters.
- Punycode is used for representing non ascii characters.
- Strip square brackets for IPV6 address.

### IsProxy

> readonly  bool IsProxy

Returns true if the server that issued this request is an http proxy. Returns false if the server is the origin server.

### MutuallyTrustedCertificates

> readonly  [`IVectorView`](/uwp/api/Windows.Foundation.Collections.IVectorView-1)&lt;[CoreWebView2ClientCertificate](corewebview2clientcertificate.md)&gt; MutuallyTrustedCertificates

Returns the list of [CoreWebView2ClientCertificate](corewebview2clientcertificate.md) when client certificate authentication is requested. The list contains mutually trusted CA certificate.

### Port

> readonly  int Port

Returns port of the server that requested client certificate authentication.

### SelectedCertificate

>  [CoreWebView2ClientCertificate](corewebview2clientcertificate.md) SelectedCertificate

Selected certificate to respond to the server.



## Methods

### GetDeferral

> [Deferral](/uwp/api/Windows.Foundation.Deferral) GetDeferral()

Gets a Deferral object.
Use this to Complete the event at a later time.






## Referenced by

- [CoreWebView2](corewebview2.md)
