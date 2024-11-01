---
title: CoreWebView2CompositionController
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/01/2024
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2CompositionController
---

# runtimeClass CoreWebView2CompositionController

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
[GetNonClientRegionAtPoint](#getnonclientregionatpoint) | 
[QueryNonClientRegion](#querynonclientregion) | 
[SendMouseInput](#sendmouseinput) | 
[SendPointerInput](#sendpointerinput) | 
[CursorChanged](#cursorchanged) | 
[NonClientRegionChanged](#nonclientregionchanged) | 

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



### GetNonClientRegionAtPoint

> [CoreWebView2NonClientRegionKind](corewebview2nonclientregionkind.md) GetNonClientRegionAtPoint([Point](/uwp/api/Windows.Foundation.Point) point)



### QueryNonClientRegion

> [`IVectorView`](/uwp/api/Windows.Foundation.Collections.IVectorView-1)&lt;[Rect](/uwp/api/Windows.Foundation.Rect)&gt; QueryNonClientRegion([CoreWebView2NonClientRegionKind](corewebview2nonclientregionkind.md) Kind)



### SendMouseInput

> void SendMouseInput([CoreWebView2MouseEventKind](corewebview2mouseeventkind.md) eventKind, [CoreWebView2MouseEventVirtualKeys](corewebview2mouseeventvirtualkeys.md) virtualKeys, uint32_t mouseData, [Point](/uwp/api/Windows.Foundation.Point) point)



### SendPointerInput

> void SendPointerInput([CoreWebView2PointerEventKind](corewebview2pointereventkind.md) eventKind, [CoreWebView2PointerInfo](corewebview2pointerinfo.md) pointerInfo)




## Events

### CursorChanged

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2CompositionController](corewebview2compositioncontroller.md), Object&gt;

### NonClientRegionChanged

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2CompositionController](corewebview2compositioncontroller.md), [CoreWebView2NonClientRegionChangedEventArgs](corewebview2nonclientregionchangedeventargs.md)&gt;

