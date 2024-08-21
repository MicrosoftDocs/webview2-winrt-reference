---
description: Indicates the error status values for web navigations.
title: CoreWebView2WebErrorStatus
ms.date: 08/26/2024
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2WebErrorStatus
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- Microsoft.Web.WebView2.Core.CoreWebView2WebErrorStatus
---

# CoreWebView2WebErrorStatus Enum

Indicates the error status values for web navigations.

| Name |  Value | Description |
|--|--|--|
|`Unknown` | 0x0  |  Indicates that an unknown error occurred.|
|`CertificateCommonNameIsIncorrect` | 0x1  |  Indicates that the SSL certificate common name does not match the web address.|
|`CertificateExpired` | 0x2  |  Indicates that the SSL certificate has expired.|
|`ClientCertificateContainsErrors` | 0x3  |  Indicates that the SSL client certificate contains errors.|
|`CertificateRevoked` | 0x4  |  Indicates that the SSL certificate has been revoked.|
|`CertificateIsInvalid` | 0x5  |  Indicates that the SSL certificate is not valid. The certificate may not match the public key pins for the host name, the certificate is signed by an untrusted authority or using a weak sign algorithm, the certificate claimed DNS names violate name constraints, the certificate contains a weak key, the validity period of the certificate is too long, lack of revocation information or revocation mechanism, non-unique host name, lack of certificate transparency information, or the certificate is chained to a [legacy Symantec root](https://security.googleblog.com/2018/03/distrust-of-symantec-pki-immediate.html).|
|`ServerUnreachable` | 0x6  |  Indicates that the host is unreachable.|
|`Timeout` | 0x7  |  Indicates that the connection has timed out.|
|`ErrorHttpInvalidServerResponse` | 0x8  |  Indicates that the server returned an invalid or unrecognized response.|
|`ConnectionAborted` | 0x9  |  Indicates that the connection was stopped.|
|`ConnectionReset` | 0xa  |  Indicates that the connection was reset.|
|`Disconnected` | 0xb  |  Indicates that the Internet connection has been lost.|
|`CannotConnect` | 0xc  |  Indicates that a connection to the destination was not established.|
|`HostNameNotResolved` | 0xd  |  Indicates that the provided host name was not able to be resolved.|
|`OperationCanceled` | 0xe  |  Indicates that the operation was canceled. This status code is also used when the app cancels a navigation via [CoreWebView2.NavigationStarting](corewebview2.md#navigationstarting) event, and for original navigation if the app navigates the WebView2 in a rapid succession away after the load for original navigation commenced, but before it completed.|
|`RedirectFailed` | 0xf  |  Indicates that the request redirect failed.|
|`UnexpectedError` | 0x10  |  An unexpected error occurred.|
|`ValidAuthenticationCredentialsRequired` | 0x11  |  Indicates that user is prompted with a login, waiting on user action. Initial navigation to a login site will always return this even if app provides credential using [CoreWebView2.BasicAuthenticationRequested](corewebview2.md#basicauthenticationrequested). HTTP response status code in this case is 401. See [status code reference](https://developer.mozilla.org/docs/Web/HTTP/Status).|
|`ValidProxyAuthenticationRequired` | 0x12  |  Indicates that user lacks proper authentication credentials for a proxy server. HTTP response status code in this case is 407. See [status code reference](https://developer.mozilla.org/docs/Web/HTTP/Status).|


## Referenced by

- [CoreWebView2NavigationCompletedEventArgs](corewebview2navigationcompletedeventargs.md)
- [CoreWebView2ServerCertificateErrorDetectedEventArgs](corewebview2servercertificateerrordetectedeventargs.md)
