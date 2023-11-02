---
description: 
title: CoreWebView2CompositionController
ms.date: 11/06/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2CompositionController
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- Microsoft.Web.WebView2.Core.CoreWebView2CompositionController
- Microsoft.Web.WebView2.Core.CoreWebView2CompositionController.Cursor
- Microsoft.Web.WebView2.Core.CoreWebView2CompositionController.RootVisualTarget
- Microsoft.Web.WebView2.Core.CoreWebView2CompositionController.CreateCoreWebView2PointerInfoFromPointerId
- Microsoft.Web.WebView2.Core.CoreWebView2CompositionController.DragEnter
- Microsoft.Web.WebView2.Core.CoreWebView2CompositionController.DragLeave
- Microsoft.Web.WebView2.Core.CoreWebView2CompositionController.DragOver
- Microsoft.Web.WebView2.Core.CoreWebView2CompositionController.Drop
- Microsoft.Web.WebView2.Core.CoreWebView2CompositionController.SendMouseInput
- Microsoft.Web.WebView2.Core.CoreWebView2CompositionController.SendPointerInput
- Microsoft.Web.WebView2.Core.CoreWebView2CompositionController.add_CursorChanged
- Microsoft.Web.WebView2.Core.CoreWebView2CompositionController.get_Cursor
- Microsoft.Web.WebView2.Core.CoreWebView2CompositionController.get_RootVisualTarget
- Microsoft.Web.WebView2.Core.CoreWebView2CompositionController.put_RootVisualTarget
- Microsoft.Web.WebView2.Core.CoreWebView2CompositionController.remove_CursorChanged
- Microsoft.Web.WebView2.Core.CoreWebView2CompositionController.CursorChanged
---

# CoreWebView2CompositionController Class

Extends: [CoreWebView2Controller](corewebview2controller.md)



## Summary

Members|Description
--|--
[Cursor](#cursor) | 
[RootVisualTarget](#rootvisualtarget) | 
[CreateCoreWebView2PointerInfoFromPointerId](#createcorewebview2pointerinfofrompointerid) | 
[DragEnter](#dragenter) | 
[DragLeave](#dragleave) | 
[DragOver](#dragover) | 
[Drop](#drop) | 
[SendMouseInput](#sendmouseinput) | 
[SendPointerInput](#sendpointerinput) | 
[CursorChanged](#cursorchanged) | 

## Properties

### Cursor

> readonly  [CoreCursor](/uwp/api/Windows.UI.Core.CoreCursor) Cursor

### RootVisualTarget

>  Object RootVisualTarget



## Methods

### CreateCoreWebView2PointerInfoFromPointerId

> [CoreWebView2PointerInfo](corewebview2pointerinfo.md) CreateCoreWebView2PointerInfoFromPointerId(uint32_t PointerId, [CoreWebView2ControllerWindowReference](corewebview2controllerwindowreference.md) ParentWindow, [Matrix4x4](/uwp/api/Windows.Foundation.Numerics.Matrix4x4) transform)



### DragEnter

> [DataPackageOperation](/uwp/api/Windows.ApplicationModel.DataTransfer.DataPackageOperation) DragEnter([CoreDragInfo](/uwp/api/Windows.ApplicationModel.DataTransfer.DragDrop.Core.CoreDragInfo) dragInfo, [CoreDragUIOverride](/uwp/api/Windows.ApplicationModel.DataTransfer.DragDrop.Core.CoreDragUIOverride) dragUIOverride)



### DragLeave

> void DragLeave()



### DragOver

> [DataPackageOperation](/uwp/api/Windows.ApplicationModel.DataTransfer.DataPackageOperation) DragOver([CoreDragInfo](/uwp/api/Windows.ApplicationModel.DataTransfer.DragDrop.Core.CoreDragInfo) dragInfo, [CoreDragUIOverride](/uwp/api/Windows.ApplicationModel.DataTransfer.DragDrop.Core.CoreDragUIOverride) dragUIOverride)



### Drop

> [DataPackageOperation](/uwp/api/Windows.ApplicationModel.DataTransfer.DataPackageOperation) Drop([CoreDragInfo](/uwp/api/Windows.ApplicationModel.DataTransfer.DragDrop.Core.CoreDragInfo) dragInfo)



### SendMouseInput

> void SendMouseInput([CoreWebView2MouseEventKind](corewebview2mouseeventkind.md) eventKind, [CoreWebView2MouseEventVirtualKeys](corewebview2mouseeventvirtualkeys.md) virtualKeys, uint32_t mouseData, [Point](/uwp/api/Windows.Foundation.Point) point)



### SendPointerInput

> void SendPointerInput([CoreWebView2PointerEventKind](corewebview2pointereventkind.md) eventKind, [CoreWebView2PointerInfo](corewebview2pointerinfo.md) pointerInfo)




## Events

### CursorChanged

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2CompositionController, Object&gt;

