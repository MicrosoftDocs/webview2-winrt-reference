---
description: Specifies the kind of sensitivity label applied to web content.
title: CoreWebView2SensitivityLabelKind
ms.date: 11/11/2026
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2SensitivityLabelKind
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2SensitivityLabelKind
---

# CoreWebView2SensitivityLabelKind Enum

Specifies the kind of sensitivity label applied to web content.
Sensitivity labels are used to classify and protect content based on its sensitivity level.

This enumeration is designed to be extensible. New values may be added in future versions. Applications should not implement a default case that assumes knowledge of all possible label kinds to ensure forward compatibility.

| Name |  Value | Description |
|--|--|--|
|`Mip` | 0x0  |  Represents a Microsoft Information Protection (MIP) sensitivity label.|
