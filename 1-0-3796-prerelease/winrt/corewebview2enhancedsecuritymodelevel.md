---
description: Enhanced Security Mode levels.
title: CoreWebView2EnhancedSecurityModeLevel
ms.date: 01/13/2026
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2EnhancedSecurityModeLevel
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2EnhancedSecurityModeLevel
---

# CoreWebView2EnhancedSecurityModeLevel Enum

Enhanced Security Mode levels.

| Name |  Value | Description |
|--|--|--|
|`Off` | 0x0  |  Enhanced Security Mode is turned off.|
|`Strict` | 0x1  |  Enhanced Security Mode is enabled in Strict level. Disables JavaScript Just-in-Time (JIT) compilation and enables additional operating system protections.

This level applies enhanced security for all sites but may reduce JavaScript performance.

See [Enhanced Security Mode](https://learn.microsoft.com/en-us/DeployEdge/microsoft-edge-security-browse-safer) for more details on what protections are enabled with this level.|


## Referenced by

- [CoreWebView2Profile](corewebview2profile.md)
