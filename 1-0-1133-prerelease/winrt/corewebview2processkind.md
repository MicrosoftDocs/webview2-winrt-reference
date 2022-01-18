---
description: Specifies the process kind used in CoreWebView2ProcessInfo.
title: CoreWebView2ProcessKind
ms.date: 01/18/2022
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ProcessKind
---

# CoreWebView2ProcessKind Enum

Specifies the process kind used in [CoreWebView2ProcessInfo](corewebview2processinfo.md).
The values in this enum make reference to the process kinds in the Chromium architecture. For more information about what these processes are and what they do, see [Browser Architecture - Inside look at modern web browser](https://developers.google.com/web/updates/2018/09/inside-browser-part1).

| Name |  Value | Description |
|--|--|--|
|`Browser` | 0x0  |  Indicates that the process is browser process.|
|`Renderer` | 0x1  |  Indicates that the process is render process.|
|`Utility` | 0x2  |  Indicates that the process is utility process.|
|`SandboxHelper` | 0x3  |  Indicates that the process is sandbox helper process.|
|`Gpu` | 0x4  |  Indicates that the process is Gpu process.|
|`PpapiPlugin` | 0x5  |  Indicates that the process is ppapi plugin process.|
|`PpapiBroker` | 0x6  |  Indicates that the process is ppapi broker process.|


## Referenced by

- [CoreWebView2ProcessInfo](corewebview2processinfo.md)
