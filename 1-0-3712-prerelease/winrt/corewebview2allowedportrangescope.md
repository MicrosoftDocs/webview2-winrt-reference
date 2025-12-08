---
description: Specifies the scope for port range restrictions.
title: CoreWebView2AllowedPortRangeScope
ms.date: 12/02/2025
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2AllowedPortRangeScope
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2AllowedPortRangeScope
---

# CoreWebView2AllowedPortRangeScope Enum

Specifies the scope for port range restrictions.

| Name |  Value | Description |
|--|--|--|
|`Default` | 0x0  |  Scope applies to all components.
This scope defines the port range restrictions that apply to all network components that do not have specific overrides. When a component-specific scope is not set, it inherits the restrictions from [CoreWebView2AllowedPortRangeScope.Default](corewebview2allowedportrangescope.md#default) scope.|
|`WebRtc` | 0x1  |  Applies only to WebRTC peer-to-peer connection.
This scope allows setting port range restrictions specifically for WebRTC connections. When set, this scope takes precedence over the [CoreWebView2AllowedPortRangeScope.Default](corewebview2allowedportrangescope.md#default) scope for WebRTC traffic.|
