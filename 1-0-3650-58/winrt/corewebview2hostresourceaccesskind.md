---
description: Kind of cross origin resource access allowed for host resources during download.
title: CoreWebView2HostResourceAccessKind
ms.date: 12/02/2025
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2HostResourceAccessKind
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2HostResourceAccessKind
---

# CoreWebView2HostResourceAccessKind Enum

Kind of cross origin resource access allowed for host resources during download.
Note that other normal access checks like same origin DOM access check and [Content Security Policy](https://developer.mozilla.org/docs/Web/HTTP/CSP) still apply.
The following table illustrates the host resource cross origin access according to access context and `CoreWebView2HostResourceAccessKind`.

Cross Origin Access Context | DENY | ALLOW | DENY_CORS
--- | --- | --- | ---
From DOM like src of img, script or iframe element| Deny | Allow | Allow
From Script like Fetch or XMLHttpRequest| Deny | Allow | Deny

| Name |  Value | Description |
|--|--|--|
|`Deny` | 0x0  |  All cross origin resource access is denied, including normal sub resource access as src of a script or image element.|
|`Allow` | 0x1  |  All cross origin resource access is allowed, including accesses that are subject to Cross-Origin Resource Sharing(CORS) check. The behavior is similar to a web site sends back http header Access-Control-Allow-Origin: *.|
|`DenyCors` | 0x2  |  Cross origin resource access is allowed for normal sub resource access like as src of a script or image element, while any access that subjects to CORS check will be denied. See [Cross-Origin Resource Sharing](https://developer.mozilla.org/docs/Web/HTTP/CORS) for more information.|


## Referenced by

- [CoreWebView2](corewebview2.md)
