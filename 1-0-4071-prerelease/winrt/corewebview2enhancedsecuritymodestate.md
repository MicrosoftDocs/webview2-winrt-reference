---
description: Enhanced Security Mode state.
title: CoreWebView2EnhancedSecurityModeState
ms.date: 06/03/2026
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2EnhancedSecurityModeState
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2EnhancedSecurityModeState
---

# CoreWebView2EnhancedSecurityModeState Enum

Enhanced Security Mode state.

| Name |  Value | Description |
|--|--|--|
|`Disabled` | 0x0  |  Enhanced Security Mode is disabled.|
|`Enabled` | 0x1  |  Enhanced Security Mode is enabled. Disables JavaScript Just-in-Time (JIT) compilation and enables additional operating system protections.

This applies enhanced security for all sites but may reduce JavaScript performance.

See [Enhanced Security Mode](https://learn.microsoft.com/en-us/DeployEdge/microsoft-edge-security-browse-safer) for more details on what protections are enabled when this state is set.|


## Referenced by

- [CoreWebView2Profile](corewebview2profile.md)
