---
title: CoreWebView2ReleaseChannels
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/30/2024
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ReleaseChannels
---

# enum CoreWebView2ReleaseChannels

Specifies the WebView2 release channel.
Use `ReleaseChannels` and `ChannelSearchKind` on `CoreWebView2EnvironmentOptions` to control which channel the WebView2 loader searches for.

|Channel|Primary purpose|How often updated with new features|
|:---:|---|:---:|
|Stable (WebView2 Runtime)|Broad Deployment|Monthly|
|Beta|Flighting with inner rings, automated testing|Monthly|
|Dev|Automated testing, selfhosting to test new APIs and features|Weekly|
|Canary|Automated testing, selfhosting to test new APIs and features|Daily|

| Name |  Value | Description |
|--|--|--|
|`None` | 0x0  |  No release channel. `ReleaseChannels` will be ignored if only this value is passed.|
|`Stable` | 0x1  |  The stable WebView2 Runtime that is released every 4 weeks.|
|`Beta` | 0x2  |  The Beta release channel that is released every 4 weeks, a week before the stable release.|
|`Dev` | 0x4  |  The Dev release channel that is released weekly.|
|`Canary` | 0x8  |  The Canary release channel that is released daily.|


## Referenced by

- [CoreWebView2EnvironmentOptions](corewebview2environmentoptions.md)
