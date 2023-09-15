---
description: This class is an extension of the CoreWebView2Controller class to support visual hosting.
title: CoreWebView2CompositionController
ms.date: 09/18/2023
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



This class is an extension of the [CoreWebView2Controller](corewebview2controller.md) class to support visual hosting.

## Summary

Members|Description
--|--
[Cursor](#cursor) | The current cursor that WebView thinks it should be.
[RootVisualTarget](#rootvisualtarget) | Gets or sets the root visual in the hosting app's visual tree.
[DragEnter](#dragenter) | Call this method to inform the CoreWebView2CompositionController that a drag operation entered the WebView2.
[DragLeave](#dragleave) | Call this method to inform the CoreWebView2CompositionController that a drag operation has left the WebView.
[DragOver](#dragover) | Call this method to inform the CoreWebView2CompositionController that a drag operation is moving over the WebView2.
[Drop](#drop) | Call this method to inform the CoreWebView2CompositionController that an object is being dropped into the WebView2.
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

### DragEnter

> [DataPackageOperation](/uwp/api/Windows.ApplicationModel.DataTransfer.DataPackageOperation) DragEnter([CoreDragInfo](/uwp/api/Windows.ApplicationModel.DataTransfer.DragDrop.Core.CoreDragInfo) dragInfo, [CoreDragUIOverride](/uwp/api/Windows.ApplicationModel.DataTransfer.DragDrop.Core.CoreDragUIOverride) dragUIOverride)

Call this method to inform the CoreWebView2CompositionController that a drag operation entered the WebView2.
Corresponds to the [ICoreDropOperationTarget.EnterAsync](/uwp/api/windows.applicationmodel.datatransfer.dragdrop.core.icoredropoperationtarget.enterasync) method when performing a drag operation into the WebView.



### DragLeave

> void DragLeave()

Call this method to inform the CoreWebView2CompositionController that a drag operation has left the WebView.
Corresponds to the [ICoreDropOperationTarget.LeaveAsync](/uwp/api/windows.applicationmodel.datatransfer.dragdrop.core.icoredropoperationtarget.leaveasync) method when performing a drag operation into the WebView.



### DragOver

> [DataPackageOperation](/uwp/api/Windows.ApplicationModel.DataTransfer.DataPackageOperation) DragOver([CoreDragInfo](/uwp/api/Windows.ApplicationModel.DataTransfer.DragDrop.Core.CoreDragInfo) dragInfo, [CoreDragUIOverride](/uwp/api/Windows.ApplicationModel.DataTransfer.DragDrop.Core.CoreDragUIOverride) dragUIOverride)

Call this method to inform the CoreWebView2CompositionController that a drag operation is moving over the WebView2.
Corresponds to the [ICoreDropOperationTarget.OverAsync](/uwp/api/windows.applicationmodel.datatransfer.dragdrop.core.icoredropoperationtarget.overasync) method when performing a drag operation into the WebView.



### Drop

> [DataPackageOperation](/uwp/api/Windows.ApplicationModel.DataTransfer.DataPackageOperation) Drop([CoreDragInfo](/uwp/api/Windows.ApplicationModel.DataTransfer.DragDrop.Core.CoreDragInfo) dragInfo)

Call this method to inform the CoreWebView2CompositionController that an object is being dropped into the WebView2.
Corresponds to the [ICoreDropOperationTarget.DropAsync](/uwp/api/windows.applicationmodel.datatransfer.dragdrop.core.icoredropoperationtarget.dropasync) method when performing a drag operation into the WebView.



### SendMouseInput

> void SendMouseInput([CoreWebView2MouseEventKind](corewebview2mouseeventkind.md) eventKind, [CoreWebView2MouseEventVirtualKeys](corewebview2mouseeventvirtualkeys.md) virtualKeys, uint32_t mouseData, [Point](/uwp/api/Windows.Foundation.Point) point)

Sends mouse input to the WebView.
If `eventKind` is [CoreWebView2MouseEventKind](corewebview2mouseeventkind.md).HorizontalWheel or [CoreWebView2MouseEventKind](corewebview2mouseeventkind.md).Wheel, then `mouseData` specifies the amount of wheel movement.
A positive value indicates that the wheel was rotated forward, away from the user; a negative value indicates that the wheel was rotated backward, toward the user. One wheel click is defined as WHEEL_DELTA, which is 120. If `eventKind` is [CoreWebView2MouseEventKind](corewebview2mouseeventkind.md).XButtonDoubleClick, [CoreWebView2MouseEventKind](corewebview2mouseeventkind.md).XButtonDown, or [CoreWebView2MouseEventKind](corewebview2mouseeventkind.md).XButtonUp, then `mouseData` specifies which X buttons were pressed or released. This value should be 1 if the first X button is pressed/released and 2 if the second X button is pressed/released. If `eventKind` is [CoreWebView2MouseEventKind](corewebview2mouseeventkind.md).Leave, then `virtualKeys`, `mouseData`, and point should all be zero. If `eventKind` is any other value, then `mouseData` should be zero. `point` is expected to be in the client coordinate space of the WebView. To track mouse events that start in the WebView and can potentially move outside of the WebView and host application, calling SetCapture and ReleaseCapture is recommended. To dismiss hover popups, it is also recommended to send [CoreWebView2MouseEventKind](corewebview2mouseeventkind.md).Leave messages.



### SendPointerInput

> void SendPointerInput([CoreWebView2PointerEventKind](corewebview2pointereventkind.md) eventKind, [CoreWebView2PointerInfo](corewebview2pointerinfo.md) pointerInfo)

Sends pen or pointer input to the WebView.
Accepts touch or pen pointer input of kinds defined in [CoreWebView2PointerEventKind](corewebview2pointereventkind.md).
Any pointer input from the system must be converted into a [CoreWebView2PointerInfo](corewebview2pointerinfo.md) first.




## Events

### CursorChanged

The event is raised when WebView thinks the cursor should be changed.
For example, when the mouse cursor is currently the default cursor but is then moved over text, it may try to change to the IBeam cursor.
It is expected for the developer to send [CoreWebView2MouseEventKind](corewebview2mouseeventkind.md).Leave messages (in addition to [CoreWebView2MouseEventKind](corewebview2mouseeventkind.md).Move messages) through [CoreWebView2CompositionController.SendMouseInput](corewebview2compositioncontroller.md#sendmouseinput). This is to ensure that the mouse is actually within the WebView that sends out CursorChanged events.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2CompositionController, Object&gt;

