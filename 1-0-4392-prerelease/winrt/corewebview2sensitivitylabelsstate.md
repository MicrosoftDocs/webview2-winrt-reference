---
description: Represents the state of sensitivity label detection and processing for web content loaded in the WebView2 control.
title: CoreWebView2SensitivityLabelsState
ms.date: 11/11/2026
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2SensitivityLabelsState
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2SensitivityLabelsState
---

# CoreWebView2SensitivityLabelsState Enum

Represents the state of sensitivity label detection and processing for web content loaded in the WebView2 control.

| Name |  Value | Description |
|--|--|--|
|`NotApplicable` | 0x0  |  Indicates that none of the loaded pages are in the allow list. Hence sensitivity labels are not applicable.|
|`Pending` | 0x1  |  Indicates that WebView2 has loaded pages from the allow list that can report sensitivity labels, but the labels are not available yet.|
|`Available` | 0x2  |  Indicates that WebView2 has loaded pages from the allow list, and the labels about the content are available now.|
