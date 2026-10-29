---
description: Event args for the CoreWebView2.NavigationStarting event.
title: CoreWebView2NavigationStartingEventArgs
ms.date: 10-29-2026
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2NavigationStartingEventArgs
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2NavigationStartingEventArgs
- CoreWebView2NavigationStartingEventArgs.AdditionalAllowedFrameAncestors
- CoreWebView2NavigationStartingEventArgs.Cancel
- CoreWebView2NavigationStartingEventArgs.IsRedirected
- CoreWebView2NavigationStartingEventArgs.IsUserInitiated
- CoreWebView2NavigationStartingEventArgs.NavigationId
- CoreWebView2NavigationStartingEventArgs.NavigationKind
- CoreWebView2NavigationStartingEventArgs.RequestHeaders
- CoreWebView2NavigationStartingEventArgs.Uri
---

# CoreWebView2NavigationStartingEventArgs Class



Event args for the [CoreWebView2.NavigationStarting](corewebview2.md#navigationstarting) event.

## Summary

Members|Description
--|--
[AdditionalAllowedFrameAncestors](#additionalallowedframeancestors) | Additional allowed frame ancestors set by the host app.
[Cancel](#cancel) | Determines whether to cancel the navigation.
[IsRedirected](#isredirected) | `true` when the navigation is redirected.
[IsUserInitiated](#isuserinitiated) | `true` when the navigation was initiated through a user gesture as opposed to programmatic navigation by page script.
[NavigationId](#navigationid) | Gets the ID of the navigation.
[NavigationKind](#navigationkind) | Gets the navigation kind of the navigation.
[RequestHeaders](#requestheaders) | Gets the HTTP request headers for the navigation.
[Uri](#uri) | Gets the uri of the requested navigation.

## Properties

### AdditionalAllowedFrameAncestors

>  string AdditionalAllowedFrameAncestors

Additional allowed frame ancestors set by the host app.

The app may set this property to allow a frame to be embedded by additional ancestors besides what is allowed by http header [X-Frame-Options](https://developer.mozilla.org/docs/Web/HTTP/Headers/X-Frame-Options) and [Content-Security-Policy frame-ancestors directive](https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Security-Policy/frame-ancestors).
If set, a frame ancestor is allowed if it is allowed by the additional allowed frame ancestors or original http header from the site.
Whether an ancestor is allowed by the additional allowed frame ancestors is done the same way as if the site provided it as the source list of the Content-Security-Policy frame-ancestors directive.
For example, if `https://example.com` and `https://www.example.com` are the origins of the top page and intermediate iframes that embed a nested site-embedding iframe, and you fully trust those origins, you should set this property to `https://example.com https://www.example.com`.

This property gives the app the ability to use iframe to embed sites that otherwise could not be embedded in an iframe in trusted app pages.
This could potentially subject the embedded sites to [Clickjacking](https://en.wikipedia.org/wiki/Clickjacking) attack from the code running in the embedding web page. Therefore, you should only set this property with origins of fully trusted embedding page and any intermediate iframes.
Whenever possible, you should use the list of specific origins of the top and intermediate frames instead of wildcard characters for this property.
This API is to provide limited support for app scenarios that used to be supported by `<webview>` element in other solutions like JavaScript UWP apps and Electron.
You should limit the usage of this property to trusted pages, and specific navigation target url, by checking the [CoreWebView2.Source](corewebview2.md#source), and [CoreWebView2NavigationStartingEventArgs.Uri](corewebview2navigationstartingeventargs.md#uri).

This property is ignored for top level document navigation.

### Cancel

>  bool Cancel

Determines whether to cancel the navigation.

If set to `true`, the navigation is no longer present and the content of the current page is intact. For performance reasons, `GET` HTTP requests may happen, while the host is responding. You may set cookies and use part of a request for the navigation. Navigations to about schemes are cancellable, unless `msWebView2CancellableAboutNavigations` feature flag is disabled. Cancellation of frame navigation to `srcdoc` is not supported and will be ignored. A cancelled navigation will fire a [CoreWebView2.NavigationCompleted](corewebview2.md#navigationcompleted) event with a [CoreWebView2NavigationCompletedEventArgs.WebErrorStatus](corewebview2navigationcompletedeventargs.md#weberrorstatus) of [CoreWebView2WebErrorStatus](corewebview2weberrorstatus.md).OperationCanceled.

### IsRedirected

> readonly  bool IsRedirected

`true` when the navigation is redirected.

### IsUserInitiated

> readonly  bool IsUserInitiated

`true` when the navigation was initiated through a user gesture as opposed to programmatic navigation by page script.
Navigations initiated via WebView2 APIs are considered as user initiated.

### NavigationId

> readonly  uint64_t NavigationId

Gets the ID of the navigation.

### NavigationKind

> readonly  [CoreWebView2NavigationKind](corewebview2navigationkind.md) NavigationKind

Gets the navigation kind of the navigation.

### RequestHeaders

> readonly  [CoreWebView2HttpRequestHeaders](corewebview2httprequestheaders.md) RequestHeaders

Gets the HTTP request headers for the navigation.

Note, you are not able to modify the HTTP request headers in a [CoreWebView2.NavigationStarting](corewebview2.md#navigationstarting) event.

### Uri

> readonly  string Uri

Gets the uri of the requested navigation.






## Referenced by

- [CoreWebView2](corewebview2.md)
- [CoreWebView2Frame](corewebview2frame.md)
