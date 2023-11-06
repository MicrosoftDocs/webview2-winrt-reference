---
description: Represents the registration of a custom scheme with the CoreWebView2Environment.
title: CoreWebView2CustomSchemeRegistration
ms.date: 11/06/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2CustomSchemeRegistration
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- Microsoft.Web.WebView2.Core.CoreWebView2CustomSchemeRegistration
- Microsoft.Web.WebView2.Core.CoreWebView2CustomSchemeRegistration.AllowedOrigins
- Microsoft.Web.WebView2.Core.CoreWebView2CustomSchemeRegistration.HasAuthorityComponent
- Microsoft.Web.WebView2.Core.CoreWebView2CustomSchemeRegistration.SchemeName
- Microsoft.Web.WebView2.Core.CoreWebView2CustomSchemeRegistration.TreatAsSecure
- Microsoft.Web.WebView2.Core.CoreWebView2CustomSchemeRegistration..ctor
- Microsoft.Web.WebView2.Core.CoreWebView2CustomSchemeRegistration.get_AllowedOrigins
- Microsoft.Web.WebView2.Core.CoreWebView2CustomSchemeRegistration.get_HasAuthorityComponent
- Microsoft.Web.WebView2.Core.CoreWebView2CustomSchemeRegistration.get_SchemeName
- Microsoft.Web.WebView2.Core.CoreWebView2CustomSchemeRegistration.get_TreatAsSecure
- Microsoft.Web.WebView2.Core.CoreWebView2CustomSchemeRegistration.put_HasAuthorityComponent
- Microsoft.Web.WebView2.Core.CoreWebView2CustomSchemeRegistration.put_TreatAsSecure
---

# CoreWebView2CustomSchemeRegistration Class



Represents the registration of a custom scheme with the [CoreWebView2Environment](corewebview2environment.md).
This allows the WebView2 app to be able to handle [CoreWebView2.WebResourceRequested](corewebview2.md#webresourcerequested) event for requests with the specified scheme and be able to navigate the WebView2 to the custom scheme. Once the environment is created, the registrations are valid and immutable throughout the lifetime of the associated WebView2s' browser process and any WebView2 environments sharing the browser process must be created with identical custom scheme registrations, otherwise the environment creation will fail.
Any further attempts to register the same scheme will fail during environment creation.
The URIs of registered custom schemes will be treated similar to http URIs for their origins.
They will have tuple origins for URIs with host and opaque origins for URIs without host as specified in [7.5 Origin - HTML Living Standard](https://html.spec.whatwg.org/multipage/origin.html).

Example:

`custom-scheme-with-host://hostname/path/to/resource` has origin of `custom-scheme-with-host://hostname`.
`custom-scheme-without-host:path/to/resource` has origin of `custom-scheme-without-host:path/to/resource`.

For [CoreWebView2.WebResourceRequested](corewebview2.md#webresourcerequested) event, the cases of request URIs and filter URIs with custom schemes will be normalized according to generic URI syntax rules. Any non-ASCII characters will be preserved.
The registered custom schemes also participate in [CORS](https://developer.mozilla.org/docs/Web/HTTP/CORS) and adheres to [CSP](https://developer.mozilla.org/docs/Web/HTTP/CSP).
The app needs to set the appropriate access headers in its [CoreWebView2.WebResourceRequested](corewebview2.md#webresourcerequested) event handler to allow CORS requests.

## Summary

Members|Description
--|--
[AllowedOrigins](#allowedorigins) | 
[HasAuthorityComponent](#hasauthoritycomponent) | Set this property to `true` if the URIs with this custom scheme will have an authority component (a host for custom schemes).
[SchemeName](#schemename) | The scheme name.
[TreatAsSecure](#treatassecure) | Whether the sites with this scheme will be treated as a [Secure Context](https://developer.mozilla.org/docs/Web/Security/Secure_Contexts) like an HTTPS site. This flag is only effective when [CoreWebView2CustomSchemeRegistration.HasAuthorityComponent](corewebview2customschemeregistration.md#hasauthoritycomponent) is also set to `true`.
CoreWebView2CustomSchemeRegistration | Initializes a new instance of the CoreWebView2CustomSchemeRegistration class.

## Properties

### AllowedOrigins

> readonly  [`IVector`](/uwp/api/Windows.Foundation.Collections.IVector-1)&lt;string&gt; AllowedOrigins

### HasAuthorityComponent

>  bool HasAuthorityComponent

Set this property to `true` if the URIs with this custom scheme will have an authority component (a host for custom schemes).
Specifically, if you have a URI of the following form you should set the `HasAuthorityComponent` value as listed.

| URI | Recommended HasAuthorityComponent value |
| -- | -- |
| `custom-scheme-with-authority://host/path` | `true` |
| `custom-scheme-without-authority:path` | `false` |

When this property is set to `true`, the URIs with this scheme will be interpreted as having a [scheme and host](https://html.spec.whatwg.org/multipage/origin.html#concept-origin-tuple) origin similar to an http URI. Note that the port and user information are never included in the computation of origins for custom schemes.
If this property is set to `false`, URIs with this scheme will have an [opaque origin](https://html.spec.whatwg.org/multipage/origin.html#concept-origin-opaque) similar to a data URI.
This property is `false` by default.
Note: For custom schemes registered as having authority component, navigations to URIs without authority of such custom schemes will fail.
However, if the content inside WebView2 references a subresource with a URI that does not have an authority component, but of a custom scheme that is registered as having authority component, the URI will be interpreted as a relative path as specified in [RFC3986](https://www.rfc-editor.org/rfc/rfc3986).
For example, `custom-scheme-with-authority:path` will be interpreted as `custom-scheme-with-authority://host/path`.
However, this behavior cannot be guaranteed to remain in future releases so it is recommended not to rely on this behavior.

### SchemeName

> readonly  string SchemeName

The scheme name.

### TreatAsSecure

>  int TreatAsSecure

Whether the sites with this scheme will be treated as a [Secure Context](https://developer.mozilla.org/docs/Web/Security/Secure_Contexts) like an HTTPS site. This flag is only effective when [CoreWebView2CustomSchemeRegistration.HasAuthorityComponent](corewebview2customschemeregistration.md#hasauthoritycomponent) is also set to `true`.
`false` by default.


## Constructors
### CoreWebView2CustomSchemeRegistration

>  CoreWebView2CustomSchemeRegistration(string schemeName)

Initializes a new instance of the CoreWebView2CustomSchemeRegistration class.





