---
description: Specifies the feature types that can be configured for origins.
title: CoreWebView2OriginFeature
ms.date: 07/27/2026
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
|`EnhancedSecurityMode` | 0x0  |  Specifies enhanced security mode settings for the origin. Enhanced Security Mode provides additional protections by disabling or restricting certain web platform features that may pose security risks, such as JIT compilation, certain JavaScript APIs, and other potentially dangerous capabilities. This feature is particularly useful for protecting against zero-day exploits and reducing attack surface. When enabled for an origin, that origin will have Enhanced Security Mode applied; when disabled, normal security mode is used. Enhanced security mode can be configured globally via [CoreWebView2Profile.EnhancedSecurityModeState](corewebview2profile.md#enhancedsecuritymodestate). If Enhanced Security Mode is not configured for an origin, the global profile setting will apply.

For more information about Enhanced Security Mode, see: [Enhanced Security Mode](https://learn.microsoft.com/en-us/microsoft-edge/webview2/concepts/security).|
|`ReputationChecking` | 0x1  |  Specifies per-origin reputation checking settings. Reputation checking protects users from phishing and malware by checking navigated URLs and downloaded files against a cloud-based reputation service. Setting this feature to `Disabled` for an origin will skip reputation checks for navigations and downloads from that origin, effectively allow-listing it. If reputation checking is not configured for an origin, the [CoreWebView2Settings.IsReputationCheckingRequired](corewebview2settings.md#isreputationcheckingrequired) setting will apply. Note: If [CoreWebView2Settings.IsReputationCheckingRequired](corewebview2settings.md#isreputationcheckingrequired) is set to `false`, setting this feature to `Enabled` for a specific origin will not re-enable reputation checks for that origin. [CoreWebView2Settings.IsReputationCheckingRequired](corewebview2settings.md#isreputationcheckingrequired) takes precedence. Warning: Disabling reputation checking for an origin bypasses phishing and malware reputation checks. Only disable for fully trusted, app-controlled origins where the content is known to be safe.|


## Referenced by

- [CoreWebView2OriginFeatureSetting](corewebview2originfeaturesetting.md)
