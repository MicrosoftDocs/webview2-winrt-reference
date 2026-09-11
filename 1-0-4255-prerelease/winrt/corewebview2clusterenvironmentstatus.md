---
description: The outcome of establishing or attaching to a shared cluster environment.
title: CoreWebView2ClusterEnvironmentStatus
ms.date: 09/03/2026
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ClusterEnvironmentStatus
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2ClusterEnvironmentStatus
---

# CoreWebView2ClusterEnvironmentStatus Enum

The outcome of establishing or attaching to a shared cluster environment.

| Name |  Value | Description |
|--|--|--|
|`Succeeded` | 0x0  |  The shared cluster environment is ready, either freshly established or attached to an existing cluster with matching options.|
|`OptionsMismatch` | 0x1  |  A cluster already exists for this ClusterName with different options.
No environment is provided. Read the cluster's options with [CoreWebView2Environment.GetClusterEnvironmentOptions](corewebview2environment.md#getclusterenvironmentoptions) and retry, or use a private environment.|
|`NotSupported` | 0x2  |  This host cannot use cluster environments, for example a sandboxed AppContainer process such as a UWP app.
No environment is provided. Use a private environment instead.
|


## Referenced by

- [CoreWebView2ClusterEnvironmentCreateResult](corewebview2clusterenvironmentcreateresult.md)
