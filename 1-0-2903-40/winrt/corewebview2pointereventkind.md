---
title: CoreWebView2PointerEventKind
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/12/2024
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2PointerEventKind
---

# enum CoreWebView2PointerEventKind

Pointer event kind used by [CoreWebView2CompositionController.SendPointerInput](corewebview2compositioncontroller.md#sendpointerinput) to convey the kind of pointer event being sent to WebView.

| Name |  Value | Description |
|--|--|--|
|`Activate` | 0x24b  |  Corresponds to `WM_POINTERACTIVATE`.|
|`Down` | 0x246  |  Corresponds to `WM_POINTERDOWN`.|
|`Enter` | 0x249  |  Corresponds to `WM_POINTERENTER`.|
|`Leave` | 0x24a  |  Corresponds to `WM_POINTERLEAVE`.|
|`Up` | 0x247  |  Corresponds to `WM_POINTERUP`.|
|`Update` | 0x245  |  Corresponds to `WM_POINTERUPDATE`.|


## Referenced by

- [CoreWebView2CompositionController](corewebview2compositioncontroller.md)
