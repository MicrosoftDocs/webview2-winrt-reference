---
description: Status of UpdateRuntime operation result.
title: CoreWebView2UpdateRuntimeStatus
ms.date: 07/28/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2UpdateRuntimeStatus
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- Microsoft.Web.WebView2.Core.CoreWebView2UpdateRuntimeStatus
---

# CoreWebView2UpdateRuntimeStatus Enum

Status of UpdateRuntime operation result.

| Name |  Value | Description |
|--|--|--|
|`LatestVersionInstalled` | 0x0  |  Latest version of Edge WebView2 Runtime is installed. No update for Edge WebView2 Runtime is available, or Edge WebView2 Runtime is updated successfully and latest version is now installed.|
|`UpdateAlreadyRunning` | 0x1  |  Edge WebView2 Runtime update is already running, which could be triggered by auto update or by other UpdateRuntime request from some app.|
|`BlockedByPolicy` | 0x2  |  Edge WebView2 Runtime update is blocked by group policy.|
|`Failed` | 0x3  |  Edge WebView2 Runtime update failed. See [CoreWebView2UpdateRuntimeResult.ExtendedError](corewebview2updateruntimeresult.md#extendederror) for more information about the failure.|


## Referenced by

- [CoreWebView2UpdateRuntimeResult](corewebview2updateruntimeresult.md)
