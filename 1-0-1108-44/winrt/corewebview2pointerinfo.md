---
description: This mostly represents a combined win32 `POINTER_INFO`, `POINTER_TOUCH_INFO`, and `POINTER_PEN_INFO` object.
title: CoreWebView2PointerInfo
ms.date: 02/10/2022
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2PointerInfo
---

# CoreWebView2PointerInfo Class



This mostly represents a combined win32 `POINTER_INFO`, `POINTER_TOUCH_INFO`, and `POINTER_PEN_INFO` object.

## Summary

Members|Description
--|--
[ButtonChangeKind](#buttonchangekind) | Gets or sets the ButtonChangeKind of the pointer event.
[DisplayRect](#displayrect) | Gets or sets the DisplayRect of the sourceDevice property of the `POINTER_INFO` struct as defined in the Windows SDK (_winuser.h_).
[FrameId](#frameid) | Gets or sets the FrameID of the pointer event.
[HimetricLocation](#himetriclocation) | Gets or sets the HimetricLocation of the pointer event.
[HimetricLocationRaw](#himetriclocationraw) | Gets or sets the HimetricLocationRaw of the pointer event.
[HistoryCount](#historycount) | Gets or sets the HistoryCount of the pointer event.
[InputData](#inputdata) | Gets or sets the InputData of the pointer event.
[KeyStates](#keystates) | Gets or sets the KeyStates of the pointer event.
[PenFlags](#penflags) | Gets or sets the PenFlags of the pointer event.
[PenMask](#penmask) | Gets or sets the PenMask of the pointer event.
[PenPressure](#penpressure) | Gets or sets the PenPressure of the pointer event.
[PenRotation](#penrotation) | Gets or sets the PenRotation of the pointer event.
[PenTiltX](#pentiltx) | Gets or sets the PenTiltX of the pointer event.
[PenTiltY](#pentilty) | Gets or sets the PenTiltY of the pointer event.
[PerformanceCount](#performancecount) | Gets or sets the PerformanceCount of the pointer event.
[PixelLocation](#pixellocation) | Gets or sets the PixelLocation of the pointer event.
[PixelLocationRaw](#pixellocationraw) | Gets or sets the PixelLocationRaw of the pointer event.
[PointerDeviceRect](#pointerdevicerect) | Gets or sets the PointerDeviceRect of the sourceDevice property of the `POINTER_INFO` struct as defined in the Windows SDK (_winuser.h_).
[PointerFlags](#pointerflags) | Gets or sets the PointerFlags of the pointer event.
[PointerId](#pointerid) | Gets or sets the PointerId of the pointer event.
[PointerKind](#pointerkind) | Gets or sets the PointerKind of the pointer event.
[Time](#time) | Gets or sets the Time of the pointer event.
[TouchContact](#touchcontact) | Gets or sets the TouchContact of the pointer event.
[TouchContactRaw](#touchcontactraw) | Gets or sets the TouchContactRaw of the pointer event.
[TouchFlags](#touchflags) | Gets or sets the TouchFlags of the pointer event.
[TouchMask](#touchmask) | Gets or sets the TouchMask of the pointer event.
[TouchOrientation](#touchorientation) | Gets or sets the TouchOrientation of the pointer event.
[TouchPressure](#touchpressure) | Gets or sets the TouchPressure of the pointer event.

## Properties

### ButtonChangeKind

>  int ButtonChangeKind

Gets or sets the ButtonChangeKind of the pointer event.
This corresponds to the ButtonChangeKind property of the `POINTER_INFO` struct. The values are defined by the `POINTER_BUTTON_CHANGE_KIND` enum in the Windows SDK (_winuser.h_).

### DisplayRect

>  [Rect](/uwp/api/Windows.Foundation.Rect) DisplayRect

Gets or sets the DisplayRect of the sourceDevice property of the `POINTER_INFO` struct as defined in the Windows SDK (_winuser.h_).

### FrameId

>  uint32_t FrameId

Gets or sets the FrameID of the pointer event.
This corresponds to the frameId property of the `POINTER_INFO` struct as defined in the Windows SDK (_winuser.h_).

### HimetricLocation

>  [Point](/uwp/api/Windows.Foundation.Point) HimetricLocation

Gets or sets the HimetricLocation of the pointer event.
This corresponds to the ptHimetricLocation property of the `POINTER_INFO` struct as defined in the Windows SDK (_winuser.h_).

### HimetricLocationRaw

>  [Point](/uwp/api/Windows.Foundation.Point) HimetricLocationRaw

Gets or sets the HimetricLocationRaw of the pointer event.
This corresponds to the ptHimetricLocationRaw property of the `POINTER_INFO` struct as defined in the Windows SDK (_winuser.h_).

### HistoryCount

>  uint32_t HistoryCount

Gets or sets the HistoryCount of the pointer event.
This corresponds to the historyCount property of the `POINTER_INFO` struct as defined in the Windows SDK (_winuser.h_).

### InputData

>  int InputData

Gets or sets the InputData of the pointer event.
This corresponds to the InputData property of the `POINTER_INFO` struct as defined in the Windows SDK (_winuser.h_).

### KeyStates

>  uint32_t KeyStates

Gets or sets the KeyStates of the pointer event.
This corresponds to the dwKeyStates property of the `POINTER_INFO` struct as defined in the Windows SDK (_winuser.h_).

### PenFlags

>  uint32_t PenFlags

Gets or sets the PenFlags of the pointer event.
This corresponds to the penFlags property of the `POINTER_PEN_INFO` struct. The values are defined by the PEN_FLAGS constants in the Windows SDK (_winuser.h_).

### PenMask

>  uint32_t PenMask

Gets or sets the PenMask of the pointer event.
This corresponds to the penMask property of the `POINTER_PEN_INFO` struct. The values are defined by the PEN_MASK constants in the Windows SDK (_winuser.h_).

### PenPressure

>  uint32_t PenPressure

Gets or sets the PenPressure of the pointer event.
This corresponds to the pressure property of the `POINTER_PEN_INFO` struct as defined in the Windows SDK (_winuser.h_).

### PenRotation

>  uint32_t PenRotation

Gets or sets the PenRotation of the pointer event.
This corresponds to the rotation property of the `POINTER_PEN_INFO` struct as defined in the Windows SDK (_winuser.h_).

### PenTiltX

>  int PenTiltX

Gets or sets the PenTiltX of the pointer event.
This corresponds to the tiltX property of the `POINTER_PEN_INFO` struct as defined in the Windows SDK (_winuser.h_).

### PenTiltY

>  int PenTiltY

Gets or sets the PenTiltY of the pointer event.
This corresponds to the tiltY property of the `POINTER_PEN_INFO` struct as defined in the Windows SDK (_winuser.h_).

### PerformanceCount

>  uint64_t PerformanceCount

Gets or sets the PerformanceCount of the pointer event.
This corresponds to the PerformanceCount property of the `POINTER_INFO` struct as defined in the Windows SDK (_winuser.h_).

### PixelLocation

>  [Point](/uwp/api/Windows.Foundation.Point) PixelLocation

Gets or sets the PixelLocation of the pointer event.
This corresponds to the ptPixelLocation property of the `POINTER_INFO` struct as defined in the Windows SDK (_winuser.h_).

### PixelLocationRaw

>  [Point](/uwp/api/Windows.Foundation.Point) PixelLocationRaw

Gets or sets the PixelLocationRaw of the pointer event.
This corresponds to the ptPixelLocationRaw property of the `POINTER_INFO` struct as defined in the Windows SDK (_winuser.h_).

### PointerDeviceRect

>  [Rect](/uwp/api/Windows.Foundation.Rect) PointerDeviceRect

Gets or sets the PointerDeviceRect of the sourceDevice property of the `POINTER_INFO` struct as defined in the Windows SDK (_winuser.h_).

### PointerFlags

>  uint32_t PointerFlags

Gets or sets the PointerFlags of the pointer event.
This corresponds to the pointerFlags property of the `POINTER_INFO` struct. The values are defined by the `POINTER_FLAGS` constants in the Windows SDK (_winuser.h_).

### PointerId

>  uint32_t PointerId

Gets or sets the PointerId of the pointer event.
This corresponds to the pointerId property of the `POINTER_INFO` struct as defined in the Windows SDK (_winuser.h_).

### PointerKind

>  uint32_t PointerKind

Gets or sets the PointerKind of the pointer event.
This corresponds to the pointerKind property of the `POINTER_INFO` struct. The values are defined by the `POINTER_INPUT_KIND` enum in the Windows SDK (_winuser.h_). Supports PT_PEN and PT_TOUCH.

### Time

>  uint32_t Time

Gets or sets the Time of the pointer event.
This corresponds to the dwTime property of the `POINTER_INFO` struct as defined in the Windows SDK (_winuser.h_).

### TouchContact

>  [Rect](/uwp/api/Windows.Foundation.Rect) TouchContact

Gets or sets the TouchContact of the pointer event.
This corresponds to the rcContact property of the `POINTER_TOUCH_INFO` struct as defined in the Windows SDK (_winuser.h_).

### TouchContactRaw

>  [Rect](/uwp/api/Windows.Foundation.Rect) TouchContactRaw

Gets or sets the TouchContactRaw of the pointer event.
This corresponds to the rcContactRaw property of the `POINTER_TOUCH_INFO` struct as defined in the Windows SDK (_winuser.h_).

### TouchFlags

>  uint32_t TouchFlags

Gets or sets the TouchFlags of the pointer event.
This corresponds to the touchFlags property of the `POINTER_TOUCH_INFO` struct. The values are defined by the TOUCH_FLAGS constants in the Windows SDK (_winuser.h_).

### TouchMask

>  uint32_t TouchMask

Gets or sets the TouchMask of the pointer event.
This corresponds to the touchMask property of the `POINTER_TOUCH_INFO` struct. The values are defined by the TOUCH_MASK constants in the Windows SDK (_winuser.h_).

### TouchOrientation

>  uint32_t TouchOrientation

Gets or sets the TouchOrientation of the pointer event.
This corresponds to the orientation property of the `POINTER_TOUCH_INFO` struct as defined in the Windows SDK (_winuser.h_).

### TouchPressure

>  uint32_t TouchPressure

Gets or sets the TouchPressure of the pointer event.
This corresponds to the pressure property of the `POINTER_TOUCH_INFO` struct as defined in the Windows SDK (_winuser.h_).






## Referenced by

- [CoreWebView2CompositionController](corewebview2compositioncontroller.md)
- [CoreWebView2Environment](corewebview2environment.md)
