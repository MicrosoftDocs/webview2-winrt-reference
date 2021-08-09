---
title: CoreWebView2CompositionController
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/12/2021
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2CompositionController
---

# runtimeClass CoreWebView2CompositionController

Extends: [CoreWebView2Controller](corewebview2controller.md)



This class is an extension of the [CoreWebView2Controller](corewebview2controller.md) class to support visual hosting.

## Summary

Members|Description
--|--
[Cursor](#cursor) | The current cursor that WebView thinks it should be.
[RootVisualTarget](#rootvisualtarget) | Gets or sets the root visual in the hosting app's visual tree.
[CreateCoreWebView2PointerInfoFromPointerId](#createcorewebview2pointerinfofrompointerid) | Converts a `PointerId` received from the system into a [CoreWebView2PointerInfo](corewebview2pointerinfo.md).
[DragEnter](#dragenter) | 
[DragLeave](#dragleave) | The drag operation has left the WebView.
[DragOver](#dragover) | The drag operation is over the WebView.
[Drop](#drop) | 
[SendMouseInput](#sendmouseinput) | Sends mouse input to the WebView.
[SendPointerInput](#sendpointerinput) | Sends pen or pointer input to the WebView.
[CursorChanged](#cursorchanged) | The event is raised when WebView thinks the cursor should be changed.

## Properties

### Cursor

> readonly  [CoreCursor](/uwp/api/Windows.UI.Core.CoreCursor) Cursor

The current cursor that WebView thinks it should be.

### RootVisualTarget

>  Object RootVisualTarget

Gets or sets the root visual in the hosting app's visual tree.

This visual is where the WebView will connect its visual tree. The app uses this visual to position the WebView within the app. The app still needs to use the [CoreWebView2Controller.Bounds](corewebview2controller.md#bounds) property to size the WebView. The RootVisualTarget property can be an IDCompositionVisual or a Windows::UI::Composition::ContainerVisual. WebView will connect its visual tree to the provided visual before returning from the property setter. The app needs to commit on its device setting the RootVisualTarget property. The RootVisualTarget property supports being set to `null` to disconnect the WebView from the app's visual tree.



## Methods

### CreateCoreWebView2PointerInfoFromPointerId

> [CoreWebView2PointerInfo](corewebview2pointerinfo.md) CreateCoreWebView2PointerInfoFromPointerId(uint32_t PointerId, [CoreWebView2ControllerWindowReference](corewebview2controllerwindowreference.md) ParentWindow, [Matrix4x4](/uwp/api/Windows.Foundation.Numerics.Matrix4x4) transform)

Converts a `PointerId` received from the system into a [CoreWebView2PointerInfo](corewebview2pointerinfo.md).
`PointerId` is the PointerId received from the system to be converted into a [CoreWebView2PointerInfo](corewebview2pointerinfo.md).
`ParentWindow` is the HWND that contains the WebView. This can be any HWND in the hwnd tree that contains the WebView.
`transform` is the transform from that HWND to the WebView.

The returned [CoreWebView2PointerInfo](corewebview2pointerinfo.md) is used in [CoreWebView2CompositionController.SendPointerInput](corewebview2compositioncontroller.md#sendpointerinput). The [CoreWebView2PointerInfo.PointerKind](corewebview2pointerinfo.md#pointerkind) must be either pen or touch or the function will fail.



### DragEnter

> uint32_t DragEnter([DataPackage](/uwp/api/Windows.ApplicationModel.DataTransfer.DataPackage) dataObject, uint32_t keyState, [Point](/uwp/api/Windows.Foundation.Point) point)



### DragLeave

> void DragLeave()

The drag operation has left the WebView.

The hosting application must register as an IDropTarget and implement and forward [DragLeave](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragleave) calls to this function. In addition the hosting application needs to create an IDropTargetHelper and call the corresponding [IDropTargetHelper::DragLeave](/windows/win32/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragleave) function on that object before forwarding the call to WebView.



### DragOver

> uint32_t DragOver(uint32_t keyState, [Point](/uwp/api/Windows.Foundation.Point) point)

The drag operation is over the WebView.

The hosting application must register as an IDropTarget and implement and forward [DragOver](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover) calls to this function. In addition, the hosting application needs to create an IDropTargetHelper and call the corresponding [IDropTargetHelper::DragOver](/windows/win32/api/shobjidl_core/nf-shobjidl_core-idroptargethelper-dragover) function on that object before forwarding the call to the WebView.
`keyState` is the keyState from `IDropTarget::DragOver`.
`point` is the point from `IDropTarget::DragOver`.
Returns a uint that is set as the effect for `IDropTarget::DragOver`.



### Drop

> uint32_t Drop([DataPackage](/uwp/api/Windows.ApplicationModel.DataTransfer.DataPackage) dataObject, uint32_t keyState, [Point](/uwp/api/Windows.Foundation.Point) point)



### SendMouseInput

> void SendMouseInput([CoreWebView2MouseEventKind](corewebview2mouseeventkind.md) eventKind, [CoreWebView2MouseEventVirtualKeys](corewebview2mouseeventvirtualkeys.md) virtualKeys, uint32_t mouseData, [Point](/uwp/api/Windows.Foundation.Point) point)

Sends mouse input to the WebView.
`eventKind` is the mouse event kind.
`virtualKeys` is the virtual keys associated with the `eventKind`.
`mouseData` is the amount of wheel movement.
`point` is the absolute position of the mouse, or the amount of motion since the last mouse event was generated, depending on the `eventKind`.

If `eventKind` is [CoreWebView2MouseEventKind](corewebview2mouseeventkind.md).HorizontalWheel or [CoreWebView2MouseEventKind](corewebview2mouseeventkind.md).Wheel, then `mouseData` specifies the amount of wheel movement.
A positive value indicates that the wheel was rotated forward, away from the user; a negative value indicates that the wheel was rotated backward, toward the user. One wheel click is defined as WHEEL_DELTA, which is 120. If `eventKind` is [CoreWebView2MouseEventKind](corewebview2mouseeventkind.md).XButtonDoubleClick, [CoreWebView2MouseEventKind](corewebview2mouseeventkind.md).XButtonDown, or [CoreWebView2MouseEventKind](corewebview2mouseeventkind.md).XButtonUp, then `mouseData` specifies which X buttons were pressed or released. This value should be 1 if the first X button is pressed/released and 2 if the second X button is pressed/released. If `eventKind` is [CoreWebView2MouseEventKind](corewebview2mouseeventkind.md).Leave, then `virtualKeys`, `mouseData`, and point should all be zero. If `eventKind` is any other value, then `mouseData` should be zero. `point` is expected to be in the client coordinate space of the WebView. To track mouse events that start in the WebView and can potentially move outside of the WebView and host application, calling SetCapture and ReleaseCapture is recommended. To dismiss hover popups, it is also recommended to send [CoreWebView2MouseEventKind](corewebview2mouseeventkind.md).Leave messages.



### SendPointerInput

> void SendPointerInput([CoreWebView2PointerEventKind](corewebview2pointereventkind.md) eventKind, [CoreWebView2PointerInfo](corewebview2pointerinfo.md) pointerInfo)

Sends pen or pointer input to the WebView.
`eventKind` is the pointer event kind.
`pointerInfo` is the pointer information.

Accepts touch or pen pointer input of kinds defined in [CoreWebView2PointerEventKind](corewebview2pointereventkind.md).
Any pointer input from the system must be converted into a [CoreWebView2PointerInfo](corewebview2pointerinfo.md) first.




## Events

### CursorChanged

The event is raised when WebView thinks the cursor should be changed.

For example, when the mouse cursor is currently the default cursor but is then moved over text, it may try to change to the IBeam cursor.
It is expected for the developer to send [CoreWebView2MouseEventKind](corewebview2mouseeventkind.md).Leave messages (in addition to [CoreWebView2MouseEventKind](corewebview2mouseeventkind.md).Move messages) through [CoreWebView2CompositionController.SendMouseInput](corewebview2compositioncontroller.md#sendmouseinput). This is to ensure that the mouse is actually within the WebView that sends out CursorChanged events.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2CompositionController](corewebview2compositioncontroller.md), Object&gt;

