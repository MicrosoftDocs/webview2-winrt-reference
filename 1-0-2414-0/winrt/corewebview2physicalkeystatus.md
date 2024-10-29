---
title: CoreWebView2PhysicalKeyStatus
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/30/2024
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2PhysicalKeyStatus
---

# struct CoreWebView2PhysicalKeyStatus

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
