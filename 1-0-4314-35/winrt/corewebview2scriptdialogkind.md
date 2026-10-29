---
description: Specifies the JavaScript dialog type used in the CoreWebView2ScriptDialogOpeningEventArgs.
title: CoreWebView2ScriptDialogKind
ms.date: 10/29/2026
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ScriptDialogKind
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2ScriptDialogKind
---

# CoreWebView2ScriptDialogKind Enum

Specifies the JavaScript dialog type used in the [CoreWebView2ScriptDialogOpeningEventArgs](corewebview2scriptdialogopeningeventargs.md).

| Name |  Value | Description |
|--|--|--|
|`Alert` | 0x0  |  Indicates that the dialog uses the `window.alert` JavaScript function.|
|`Confirm` | 0x1  |  Indicates that the dialog uses the `window.confirm` JavaScript function.|
|`Prompt` | 0x2  |  Indicates that the dialog uses the `window.prompt` JavaScript function.|
|`Beforeunload` | 0x3  |  Indicates that the dialog uses the `beforeunload` JavaScript event.|


## Referenced by

- [CoreWebView2ScriptDialogOpeningEventArgs](corewebview2scriptdialogopeningeventargs.md)
