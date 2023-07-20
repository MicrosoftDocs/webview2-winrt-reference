---
description: Indicates the kind of context for which the context menu was created for the CoreWebView2ContextMenuTarget.Kind property. This enum will always represent the active element that caused the context menu request. If there is a selection with multiple images, audio and text, for example, the element that the end user right clicks on within this selection will be the option represented by this enum.
title: CoreWebView2ContextMenuTargetKind
ms.date: 07/24/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ContextMenuTargetKind
---

# CoreWebView2ContextMenuTargetKind Enum

Indicates the kind of context for which the context menu was created for the [CoreWebView2ContextMenuTarget.Kind](corewebview2contextmenutarget.md#kind) property. This enum will always represent the active element that caused the context menu request. If there is a selection with multiple images, audio and text, for example, the element that the end user right clicks on within this selection will be the option represented by this enum.

| Name |  Value | Description |
|--|--|--|
|`Page` | 0x0  |  Indicates that the context menu was created for the page without any additional content.|
|`Image` | 0x1  |  Indicates that the context menu was created for an image element.|
|`SelectedText` | 0x2  |  Indicates that the context menu was created for selected text.|
|`Audio` | 0x3  |  Indicates that the context menu was created for an audio element.|
|`Video` | 0x4  |  Indicates that the context menu was created for a video element.|


## Referenced by

- [CoreWebView2ContextMenuTarget](corewebview2contextmenutarget.md)
