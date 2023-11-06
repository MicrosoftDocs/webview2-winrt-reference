---
description: Event args for the CoreWebView2.NavigationStarting event.
title: CoreWebView2NavigationStartingEventArgs
ms.date: 11/06/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2NavigationStartingEventArgs
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs
- Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs.AdditionalAllowedFrameAncestors
- Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs.Cancel
- Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs.IsRedirected
- Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs.IsUserInitiated
- Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs.NavigationId
- Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs.NavigationKind
- Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs.RequestHeaders
- Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs.Uri
- Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs.get_AdditionalAllowedFrameAncestors
- Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs.get_Cancel
- Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs.get_IsRedirected
- Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs.get_IsUserInitiated
- Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs.get_NavigationId
- Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs.get_NavigationKind
- Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs.get_RequestHeaders
- Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs.get_Uri
- Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs.put_AdditionalAllowedFrameAncestors
- Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs.put_Cancel
---

# CoreWebView2NavigationStartingEventArgs Class



Event args for the [CoreWebView2.NavigationStarting](corewebview2.md#navigationstarting) event.

## Summary

Members|Description
--|--
[AdditionalAllowedFrameAncestors](#additionalallowedframeancestors) | Additional allowed frame ancestors set by the host app.
[Cancel](#cancel) | Determines whether to cancel the navigation.
[IsRedirected](#isredirected) | `true` when the navigation is redirected.
[IsUserInitiated](#isuserinitiated) | `true` when the new window request was initiated through a user gesture.
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
This could potentially subject the embedded sites to [Clickjacking](https://wikipedia.org/wiki/Clickjacking) attack from the code running in the embedding web page. Therefore, you should only set this property with origins of fully trusted embedding page and any intermediate iframes.
Whenever possible, you should use the list of specific origins of the top and intermediate frames instead of wildcard characters for this property.
This API is to provide limited support for app scenarios that used to be supported by `&lt;webview&gt;` element in other solutions like JavaScript UWP apps and Electron.
You should limit the usage of this property to trusted pages, and specific navigation target url, by checking the [CoreWebView2.Source](corewebview2.md#source), and [CoreWebView2NavigationStartingEventArgs.Uri](corewebview2navigationstartingeventargs.md#uri).

This property is ignored for top level document navigation.

### Cancel

>  bool Cancel

Determines whether to cancel the navigation.
If set to `true`, the navigation is no longer present and the content of the current page is intact. For performance reasons, `GET` HTTP requests may happen, while the host is responding. You may set cookies and use part of a request for the navigation. Cancellation for navigation to `about:blank` or frame navigation to srcdoc is not supported and ignored.

### IsRedirected

> readonly  bool IsRedirected

`true` when the navigation is redirected.

### IsUserInitiated

> readonly  bool IsUserInitiated

`true` when the new window request was initiated through a user gesture.
Examples of user initiated requests are:
- Selecting an anchor tag with target
- Programmatic window open from a script that directly run as a result of user interaction such as via onclick handlers.
Non-user initiated requests are programmatic window opens from a script that are not directly triggered by user interaction, such as those that run while loading a new page or via timers.
The Microsoft Edge popup blocker is disabled for WebView so the app is able to use this flag to block non-user initiated popups.

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
