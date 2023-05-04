---
title: CoreWebView2MouseEventVirtualKeys
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2023
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2MouseEventVirtualKeys
---

# enum CoreWebView2MouseEventVirtualKeys

Mouse event virtual keys associated with a [CoreWebView2MouseEventKind](corewebview2mouseeventkind.md) for [CoreWebView2CompositionController.SendMouseInput](corewebview2compositioncontroller.md#sendmouseinput).

| Name |  Value | Description |
|--|--|--|
|`None` | 0x0  |  No additional keys pressed.|
|`LeftButton` | 0x1  |  Left mouse button is down, `MK_LBUTTON`.|
|`RightButton` | 0x2  |  Right mouse button is down, `MK_RBUTTON`.|
|`Shift` | 0x4  |  Shift key is down, `MK_SHIFT`.|
|`Control` | 0x8  |  Ctrl key is down, `MK_CONTROL`.|
|`MiddleButton` | 0x10  |  Middle mouse button is down, `MK_MBUTTON`.|
|`XButton1` | 0x20  |  First X button is down, `MK_XBUTTON1`.|
|`XButton2` | 0x40  |  Second X button is down, `MK_XBUTTON2`.|


## Referenced by

- [CoreWebView2CompositionController](corewebview2compositioncontroller.md)
