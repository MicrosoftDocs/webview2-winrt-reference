---
description: Specifies the key event kind that raises an CoreWebView2Controller.AcceleratorKeyPressed event.
title: CoreWebView2KeyEventKind
ms.date: 02/10/2022
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2KeyEventKind
---

# CoreWebView2KeyEventKind Enum

Specifies the key event kind that raises an [CoreWebView2Controller.AcceleratorKeyPressed](corewebview2controller.md#acceleratorkeypressed) event.

| Name |  Value | Description |
|--|--|--|
|`KeyDown` | 0x0  |  Specifies that the key event kind corresponds to window message `WM_KEYDOWN`.|
|`KeyUp` | 0x1  |  Specifies that the key event kind corresponds to window message `WM_KEYUP`.|
|`SystemKeyDown` | 0x2  |  Specifies that the key event kind corresponds to window message `WM_SYSKEYDOWN`.|
|`SystemKeyUp` | 0x3  |  Specifies that the key event kind corresponds to window message `WM_SYSKEYUP`.|


## Referenced by

- [CoreWebView2AcceleratorKeyPressedEventArgs](corewebview2acceleratorkeypressedeventargs.md)
