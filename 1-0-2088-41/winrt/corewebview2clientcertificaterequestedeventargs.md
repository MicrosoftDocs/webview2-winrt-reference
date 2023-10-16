---
description: 
title: CoreWebView2ClientCertificateRequestedEventArgs
ms.date: 10/16/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ClientCertificateRequestedEventArgs
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- Microsoft.Web.WebView2.Core.CoreWebView2ClientCertificateRequestedEventArgs
- Microsoft.Web.WebView2.Core.CoreWebView2ClientCertificateRequestedEventArgs.AllowedCertificateAuthorities
- Microsoft.Web.WebView2.Core.CoreWebView2ClientCertificateRequestedEventArgs.Cancel
- Microsoft.Web.WebView2.Core.CoreWebView2ClientCertificateRequestedEventArgs.Handled
- Microsoft.Web.WebView2.Core.CoreWebView2ClientCertificateRequestedEventArgs.Host
- Microsoft.Web.WebView2.Core.CoreWebView2ClientCertificateRequestedEventArgs.IsProxy
- Microsoft.Web.WebView2.Core.CoreWebView2ClientCertificateRequestedEventArgs.MutuallyTrustedCertificates
- Microsoft.Web.WebView2.Core.CoreWebView2ClientCertificateRequestedEventArgs.Port
- Microsoft.Web.WebView2.Core.CoreWebView2ClientCertificateRequestedEventArgs.SelectedCertificate
- Microsoft.Web.WebView2.Core.CoreWebView2ClientCertificateRequestedEventArgs.GetDeferral
- Microsoft.Web.WebView2.Core.CoreWebView2ClientCertificateRequestedEventArgs.get_AllowedCertificateAuthorities
- Microsoft.Web.WebView2.Core.CoreWebView2ClientCertificateRequestedEventArgs.get_Cancel
- Microsoft.Web.WebView2.Core.CoreWebView2ClientCertificateRequestedEventArgs.get_Handled
- Microsoft.Web.WebView2.Core.CoreWebView2ClientCertificateRequestedEventArgs.get_Host
- Microsoft.Web.WebView2.Core.CoreWebView2ClientCertificateRequestedEventArgs.get_IsProxy
- Microsoft.Web.WebView2.Core.CoreWebView2ClientCertificateRequestedEventArgs.get_MutuallyTrustedCertificates
- Microsoft.Web.WebView2.Core.CoreWebView2ClientCertificateRequestedEventArgs.get_Port
- Microsoft.Web.WebView2.Core.CoreWebView2ClientCertificateRequestedEventArgs.get_SelectedCertificate
- Microsoft.Web.WebView2.Core.CoreWebView2ClientCertificateRequestedEventArgs.put_Cancel
- Microsoft.Web.WebView2.Core.CoreWebView2ClientCertificateRequestedEventArgs.put_Handled
- Microsoft.Web.WebView2.Core.CoreWebView2ClientCertificateRequestedEventArgs.put_SelectedCertificate
---

# CoreWebView2ClientCertificateRequestedEventArgs Class



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
