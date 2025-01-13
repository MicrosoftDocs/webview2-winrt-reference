---
title: CoreWebView2ScriptDialogKind
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/13/2025
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ScriptDialogKind
---

# enum CoreWebView2ScriptDialogKind

Specifies the JavaScript dialog kind used in [CoreWebView2ScriptDialogOpeningEventArgs](corewebview2scriptdialogopeningeventargs.md).

| Name |  Value | Description |
|--|--|--|
|`Alert` | 0x0  |  Indicates that the dialog uses `window.alert` JavaScript function.|
|`Confirm` | 0x1  |  Indicates that the dialog uses `window.confirm` JavaScript function.|
|`Prompt` | 0x2  |  Indicates that the dialog uses `window.prompt` JavaScript function.|
|`Beforeunload` | 0x3  |  Indicates that the dialog uses `window.beforeunload` JavaScript event.
|


## Referenced by

- [CoreWebView2ScriptDialogOpeningEventArgs](corewebview2scriptdialogopeningeventargs.md)
