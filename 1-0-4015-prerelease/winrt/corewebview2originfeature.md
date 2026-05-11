---
description: Specifies the feature types that can be configured for origins.
title: CoreWebView2OriginFeature
ms.date: 05/04/2026
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2OriginFeature
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2OriginFeature
---

# CoreWebView2OriginFeature Enum

Specifies the feature types that can be configured for origins.

| Name |  Value | Description |
|--|--|--|
|`EnhancedSecurityMode` | 0x0  |  Specifies enhanced security mode settings for the origin. Enhanced Security Mode provides additional protections by disabling or restricting certain web platform features that may pose security risks, such as JIT compilation, certain JavaScript APIs, and other potentially dangerous capabilities. This feature is particularly useful for protecting against zero-day exploits and reducing attack surface. When enabled for an origin, that origin will have Enhanced Security Mode applied; when disabled, normal security mode is used. Enhanced security mode can be configured globally via [CoreWebView2Profile.EnhancedSecurityModeLevel](corewebview2profile.md#enhancedsecuritymodelevel). If Enhanced Security Mode is not configured for an origin, the global profile setting will apply.

For more information about Enhanced Security Mode, see: [Enhanced Security Mode](https://learn.microsoft.com/en-us/microsoft-edge/webview2/concepts/security).|


## Referenced by

- [CoreWebView2OriginFeatureSetting](corewebview2originfeaturesetting.md)
