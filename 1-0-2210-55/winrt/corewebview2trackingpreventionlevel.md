---
description: Tracking prevention levels.
title: CoreWebView2TrackingPreventionLevel
ms.date: 12/11/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2TrackingPreventionLevel
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- Microsoft.Web.WebView2.Core.CoreWebView2TrackingPreventionLevel
---

# CoreWebView2TrackingPreventionLevel Enum

Tracking prevention levels.

| Name |  Value | Description |
|--|--|--|
|`None` | 0x0  |  Tracking prevention is turned off.|
|`Basic` | 0x1  |  The least restrictive level of tracking prevention. Set to this level to protect against malicious trackers but allows most other trackers and personalize content and ads. See [Current tracking prevention behavior](/microsoft-edge/web-platform/tracking-prevention#current-tracking-prevention-behavior) for fine-grained information on what is being blocked with this level and can change with different Edge versions.|
|`Balanced` | 0x2  |  The default level of tracking prevention. Set to this level to protect against social media tracking on top of malicious trackers. Content and ads will likely be less personalized. See [Current tracking prevention behavior](/microsoft-edge/web-platform/tracking-prevention#current-tracking-prevention-behavior) for fine-grained information on what is being blocked with this level and can change with different Edge versions.|
|`Strict` | 0x3  |  The most restrictive level of tracking prevention. Set to this level to protect against malicious trackers and most trackers across sites. Content and ads will likely have minimal personalization. This level blocks the most trackers but could cause some websites to not behave as expected. See [Current tracking prevention behavior](/microsoft-edge/web-platform/tracking-prevention#current-tracking-prevention-behavior) for fine-grained information on what is being blocked with this level and can change with different Edge versions.|


## Referenced by

- [CoreWebView2Profile](corewebview2profile.md)
