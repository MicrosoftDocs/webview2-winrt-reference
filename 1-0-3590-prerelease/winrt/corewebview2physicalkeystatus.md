---
description: Contains the information packed into the LPARAM sent to a Win32 key event.
title: CoreWebView2PhysicalKeyStatus
ms.date: 10/01/2025
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2PhysicalKeyStatus
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2PhysicalKeyStatus
---

# CoreWebView2PhysicalKeyStatus Struct

Contains the information packed into the LPARAM sent to a Win32 key event.
For more information about `WM_KEYDOWN`, navigate to [WM_KEYDOWN message](/windows/win32/inputdev/wm-keydown).

## Fields
| Name | Type | Description |
|---|---|---|
| IsExtendedKey | int | Indicates that the key is an extended key. |
| IsKeyReleased | int | Indicates that the key was released. |
| IsMenuKeyDown | int | Indicates that a menu key is held down (context code). |
| RepeatCount | uint32_t | Specifies the repeat count for the current message. |
| ScanCode | uint32_t | Specifies the scan code. |
| WasKeyDown | int | Indicates that the key was held down. |


## Referenced by

- [CoreWebView2AcceleratorKeyPressedEventArgs](corewebview2acceleratorkeypressedeventargs.md)
