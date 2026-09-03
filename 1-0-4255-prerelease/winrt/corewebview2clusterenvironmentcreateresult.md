---
description: The result of establishing or attaching to a shared cluster environment.
title: CoreWebView2ClusterEnvironmentCreateResult
ms.date: 09/03/2026
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ClusterEnvironmentCreateResult
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2ClusterEnvironmentCreateResult
- CoreWebView2ClusterEnvironmentCreateResult.Environment
- CoreWebView2ClusterEnvironmentCreateResult.Status
---

# CoreWebView2ClusterEnvironmentCreateResult Class



The result of establishing or attaching to a shared cluster environment.

## Summary

Members|Description
--|--
[Environment](#environment) | The shared cluster environment. Non-null only when [CoreWebView2ClusterEnvironmentCreateResult.Status](corewebview2clusterenvironmentcreateresult.md#status) is `Succeeded`.
[Status](#status) | The outcome of the operation.

## Properties

### Environment

> readonly  [CoreWebView2Environment](corewebview2environment.md) Environment

The shared cluster environment. Non-null only when [CoreWebView2ClusterEnvironmentCreateResult.Status](corewebview2clusterenvironmentcreateresult.md#status) is `Succeeded`.

### Status

> readonly  [CoreWebView2ClusterEnvironmentStatus](corewebview2clusterenvironmentstatus.md) Status

The outcome of the operation.




