---
description: Tracking prevention levels.
title: CoreWebView2TrackingPreventionLevel
ms.date: 06/03/2026
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2TrackingPreventionLevel
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2TrackingPreventionLevel
---

# CoreWebView2TrackingPreventionLevel Enum

Tracking prevention levels.

| Name |  Value | Description |
|--|--|--|
|`None` | 0x0  |  Tracking prevention is turned off.|
|`Basic` | 0x1  |  The least restrictive level of tracking prevention. Set to this level to protect against malicious trackers but allows most other trackers and personalize content and ads. See [Current tracking prevention behavior](/microsoft-edge/web-platform/tracking-prevention#current-tracking-prevention-behavior) for fine-grained information on what is being blocked with this level and can change with different Edge versions.|
|`Balanced` | 0x2  |  The default level of tracking prevention. Set to this level to protect against social media tracking on top of malicious trackers. Content and ads will likely be less personalized. See [Current tracking prevention behavior](/microsoft-edge/web-platform/tracking-prevention#current-tracking-prevention-behavior) for fine-grained information on what is being blocked with this level and can change with different Edge versions.|
|`Strict` | 0x3  |  The most restrictive level of tracking prevention. Set to this level to protect against malicious trackers and most trackers across sites. Content and ads will likely have minimal personalization. This level blocks the most trackers but could cause some websites to not behave as expected. See [Current tracking prevention behavior](/microsoft-edge/web-platform/tracking-prevention#current-tracking-prevention-behavior) for fine-grained information on what is being blocked with this level and can change with different Edge versions.

The configuration is not persisted to the user data folder. The property is reset when the profile is recreated.

The default value is [CoreWebView2EnhancedSecurityModeLevel.Off](corewebview2enhancedsecuritymodelevel.md#off).

When set to `Off`, Enhanced Security Mode is disabled. When set to `Strict`, the Enhanced Security Mode feature is enabled in Strict level.

See [CoreWebView2EnhancedSecurityModeLevel](corewebview2enhancedsecuritymodelevel.md) for descriptions of levels.
Changes apply immediately to new navigation. Existing pages require a reload for the change to take effect.

The EnhancedSecurityModeLevel setting is not persisted in the user data folder. It resets to the default value of [CoreWebView2EnhancedSecurityModeLevel](corewebview2enhancedsecuritymodelevel.md).Off when the profile is destroyed and recreated.|


## Referenced by

- [CoreWebView2Profile](corewebview2profile.md)
