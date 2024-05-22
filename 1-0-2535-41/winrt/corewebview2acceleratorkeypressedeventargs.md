---
description: Event args for the CoreWebView2Controller.AcceleratorKeyPressed event.
title: CoreWebView2AcceleratorKeyPressedEventArgs
ms.date: 05/28/2024
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2AcceleratorKeyPressedEventArgs
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- Microsoft.Web.WebView2.Core.CoreWebView2AcceleratorKeyPressedEventArgs
- Microsoft.Web.WebView2.Core.CoreWebView2AcceleratorKeyPressedEventArgs.Handled
- Microsoft.Web.WebView2.Core.CoreWebView2AcceleratorKeyPressedEventArgs.IsBrowserAcceleratorKeyEnabled
- Microsoft.Web.WebView2.Core.CoreWebView2AcceleratorKeyPressedEventArgs.KeyEventKind
- Microsoft.Web.WebView2.Core.CoreWebView2AcceleratorKeyPressedEventArgs.KeyEventLParam
- Microsoft.Web.WebView2.Core.CoreWebView2AcceleratorKeyPressedEventArgs.PhysicalKeyStatus
- Microsoft.Web.WebView2.Core.CoreWebView2AcceleratorKeyPressedEventArgs.VirtualKey
- Microsoft.Web.WebView2.Core.CoreWebView2AcceleratorKeyPressedEventArgs.get_Handled
- Microsoft.Web.WebView2.Core.CoreWebView2AcceleratorKeyPressedEventArgs.get_IsBrowserAcceleratorKeyEnabled
- Microsoft.Web.WebView2.Core.CoreWebView2AcceleratorKeyPressedEventArgs.get_KeyEventKind
- Microsoft.Web.WebView2.Core.CoreWebView2AcceleratorKeyPressedEventArgs.get_KeyEventLParam
- Microsoft.Web.WebView2.Core.CoreWebView2AcceleratorKeyPressedEventArgs.get_PhysicalKeyStatus
- Microsoft.Web.WebView2.Core.CoreWebView2AcceleratorKeyPressedEventArgs.get_VirtualKey
- Microsoft.Web.WebView2.Core.CoreWebView2AcceleratorKeyPressedEventArgs.put_Handled
- Microsoft.Web.WebView2.Core.CoreWebView2AcceleratorKeyPressedEventArgs.put_IsBrowserAcceleratorKeyEnabled
---

# CoreWebView2AcceleratorKeyPressedEventArgs Class



Event args for the [CoreWebView2Controller.AcceleratorKeyPressed](corewebview2controller.md#acceleratorkeypressed) event.

## Summary

Members|Description
--|--
[Handled](#handled) | Indicates whether the [CoreWebView2Controller.AcceleratorKeyPressed](corewebview2controller.md#acceleratorkeypressed) event is handled by host.
[IsBrowserAcceleratorKeyEnabled](#isbrowseracceleratorkeyenabled) | This `IsBrowserAcceleratorKeyEnabled` property allows developers to control whether the browser handles accelerator keys such as Ctrl+P or F3, etc.
[KeyEventKind](#keyeventkind) | Gets the key event kind that caused the event to run.
[KeyEventLParam](#keyeventlparam) | Gets the LPARAM value that accompanied the window message.
[PhysicalKeyStatus](#physicalkeystatus) | Gets a [CoreWebView2PhysicalKeyStatus](corewebview2physicalkeystatus.md) representing the information passed in the LPARAM of the window message.
[VirtualKey](#virtualkey) | Gets the Win32 virtual key code of the key that was pressed or released.

## Properties

### Handled

>  bool Handled

Indicates whether the [CoreWebView2Controller.AcceleratorKeyPressed](corewebview2controller.md#acceleratorkeypressed) event is handled by host.

For browser accelerator keys, when an accelerator key is pressed, the propagation and processing order is:

1. A CoreWebView2Controller.AcceleratorKeyPressed event is raised
1. WebView2 browser feature accelerator key handling
1. Web Content Handling: If the key combination isn't reserved for browser actions, the key event propagates to the web content, where JavaScript event listeners can capture and respond to it.

If `Handled` property is set to `true` anywhere along the path, the event propagation stops, and web content will not receive the key and this prevents the WebView from performing the default action for this accelerator key. Otherwise the WebView will perform the default action for the accelerator key.

### IsBrowserAcceleratorKeyEnabled

>  bool IsBrowserAcceleratorKeyEnabled

This `IsBrowserAcceleratorKeyEnabled` property allows developers to control whether the browser handles accelerator keys such as Ctrl+P or F3, etc.
The `CoreWebView2Settings.AreBrowserAcceleratorKeysEnabled` API is a convenient setting for developers to disable all the browser accelerator keys together. This setting also sets the default value for the `IsBrowserAcceleratorKeyEnabled` property.

By default, `CoreWebView2Settings.AreBrowserAcceleratorKeysEnabled` is `TRUE` and `IsBrowserAcceleratorKeyEnabled` is `TRUE`. When developers change `CoreWebView2Settings.AreBrowserAcceleratorKeysEnabled` setting to `FALSE`, this will change default value for `IsBrowserAcceleratorKeyEnabled` to `FALSE`. If developers want specific keys to be handled by the browser after changing the `CoreWebView2Settings.AreBrowserAcceleratorKeysEnabled` setting to `FALSE`, they need to enable these keys by setting `IsBrowserAcceleratorKeyEnabled` to `TRUE`.

The `CoreWebView2Controller.AcceleratorKeyPressed` event is raised any time an accelerator key is pressed, regardless of whether accelerator keys are enabled or not.

This API will give the event arg higher priority over the `CoreWebView2Settings.AreBrowserAcceleratorKeysEnabled` setting when we handle the keys.

With `IsBrowserAcceleratorKeyEnabled` property, if developers mark `IsBrowserAcceleratorKeyEnabled` as `FALSE`, the browser will skip the WebView2 browser feature accelerator key handling process, but the event propagation continues, and web content will receive the key combination.

This property does not disable accelerator keys related to movement and text editing, such as:
 - Home, End, Page Up, and Page Down
 - Ctrl-X, Ctrl-C, Ctrl-V
 - Ctrl-A for Select All
 - Ctrl-Z for Undo

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
