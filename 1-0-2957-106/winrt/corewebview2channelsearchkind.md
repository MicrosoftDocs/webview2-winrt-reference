---
title: CoreWebView2ChannelSearchKind
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/13/2025
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ChannelSearchKind
---

# enum CoreWebView2ChannelSearchKind

The order that release channels are searched for during environment creation.
The default behavior is to search for and use the most stable channel found on the device. The order from most to least stable is: WebView2 Runtime -> Beta -> Dev -> Canary. Switch the order to prefer the least stable channel in order to perform pre-release testing. See [CoreWebView2ReleaseChannels](corewebview2releasechannels.md) for descriptions of channels.

| Name |  Value | Description |
|--|--|--|
|`MostStable` | 0x0  |  Search for a release channel from most to least stable: WebView2 Runtime -> Beta -> Dev -> Canary. This is the default behavior.|
|`LeastStable` | 0x1  |  Search for a release channel from least to most stable: Canary -> Dev -> Beta -> WebView2 Runtime.|


## Referenced by

- [CoreWebView2EnvironmentOptions](corewebview2environmentoptions.md)
