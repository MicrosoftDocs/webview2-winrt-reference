---
description: Event args for the CoreWebView2Controller.AcceleratorKeyPressed event.
title: CoreWebView2AcceleratorKeyPressedEventArgs
ms.date: 01/17/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2AcceleratorKeyPressedEventArgs
---

# CoreWebView2AcceleratorKeyPressedEventArgs Class



Event args for the [CoreWebView2Controller.AcceleratorKeyPressed](corewebview2controller.md#acceleratorkeypressed) event.

## Summary

Members|Description
--|--
[Handled](#handled) | Indicates whether the [CoreWebView2Controller.AcceleratorKeyPressed](corewebview2controller.md#acceleratorkeypressed) event is handled by host.
[KeyEventKind](#keyeventkind) | Gets the key event kind that caused the event to run.
[KeyEventLParam](#keyeventlparam) | Gets the LPARAM value that accompanied the window message.
[PhysicalKeyStatus](#physicalkeystatus) | Gets a [CoreWebView2PhysicalKeyStatus](corewebview2physicalkeystatus.md) representing the information passed in the LPARAM of the window message.
[VirtualKey](#virtualkey) | Gets the Win32 virtual key code of the key that was pressed or released.

## Properties

### Handled

>  bool Handled

Indicates whether the [CoreWebView2Controller.AcceleratorKeyPressed](corewebview2controller.md#acceleratorkeypressed) event is handled by host.
If set to `true` then this prevents the WebView from performing the default action for this accelerator key. Otherwise the WebView will perform the default action for the accelerator key.

### KeyEventKind

> readonly  [CoreWebView2KeyEventKind](corewebview2keyeventkind.md) KeyEventKind

Gets the key event kind that caused the event to run.

### KeyEventLParam

> readonly  int KeyEventLParam

Gets the LPARAM value that accompanied the window message.
See the documentation for the `WM_KEYDOWN` and `WM_KEYUP` messages.

### PhysicalKeyStatus

> readonly  [CoreWebView2PhysicalKeyStatus](corewebview2physicalkeystatus.md) PhysicalKeyStatus

Gets a [CoreWebView2PhysicalKeyStatus](corewebview2physicalkeystatus.md) representing the information passed in the LPARAM of the window message.

### VirtualKey

> readonly  uint32_t VirtualKey

Gets the Win32 virtual key code of the key that was pressed or released.
It is one of the Win32 virtual key constants such as VK_RETURN or an (uppercase) ASCII value such as 'A'. Verify whether Ctrl or Alt are pressed by running GetKeyState(VK_CONTROL) or GetKeyState(VK_MENU).






## Referenced by

- [CoreWebView2Controller](corewebview2controller.md)
