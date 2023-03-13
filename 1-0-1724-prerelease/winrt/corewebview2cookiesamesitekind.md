---
description: Kind of cookie SameSite status used in the CoreWebView2Cookie class.
title: CoreWebView2CookieSameSiteKind
ms.date: 03/13/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2CookieSameSiteKind
---

# CoreWebView2CookieSameSiteKind Enum

Kind of cookie SameSite status used in the [CoreWebView2Cookie](corewebview2cookie.md) class.
These fields match those as specified in https://developer.mozilla.org/docs/Web/HTTP/Cookies#.
Learn more about SameSite cookies here: https://tools.ietf.org/html/draft-west-first-party-cookies-07

| Name |  Value | Description |
|--|--|--|
|`None` | 0x0  |  None SameSite type. No restrictions on cross-site requests.|
|`Lax` | 0x1  |  Lax SameSite type. The cookie will be sent with "same-site" requests, and with "cross-site" top level navigation.|
|`Strict` | 0x2  |  Strict SameSite type. The cookie will only be sent along with "same-site" requests.|


## Referenced by

- [CoreWebView2Cookie](corewebview2cookie.md)
