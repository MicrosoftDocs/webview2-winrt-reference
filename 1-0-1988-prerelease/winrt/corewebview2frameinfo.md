---
description: Provides a set of properties for a frame in the CoreWebView2.
title: CoreWebView2FrameInfo
ms.date: 07/24/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2FrameInfo
---

# CoreWebView2FrameInfo Class



Provides a set of properties for a frame in the [CoreWebView2](corewebview2.md).

## Summary

Members|Description
--|--
[FrameId](#frameid) | The unique identifier of the frame associated with the current CoreWebView2FrameInfo. It's the same kind of ID as with the [CoreWebView2.FrameId](corewebview2.md#frameid) and [CoreWebView2Frame.FrameId](corewebview2frame.md#frameid). FrameId will only be populated when obtained calling [CoreWebView2ProcessInfo.AssociatedFrameInfos](corewebview2processinfo.md#associatedframeinfos). CoreWebView2FrameInfo objects obtained via [CoreWebView2.ProcessFailed](corewebview2.md#processfailed) will always have an invalid frame Id `0`.
[FrameKind](#framekind) | Gets the kind of the frame. FrameKind will only be populated when obtained calling [CoreWebView2ProcessInfo.AssociatedFrameInfos](corewebview2processinfo.md#associatedframeinfos). CoreWebView2FrameInfo objects obtained via [CoreWebView2.ProcessFailed](corewebview2.md#processfailed) will always have the default value [CoreWebView2FrameKind.Other](corewebview2framekind.md#other).
[Name](#name) | Gets the name attribute of the frame, as in `<iframe name="frame-name" ...>`.
[ParentFrameInfo](#parentframeinfo) | This frame's parent frame's CoreWebView2FrameInfo. ParentFrameInfo will only be populated when obtained via calling [CoreWebView2ProcessInfo.AssociatedFrameInfos](corewebview2processinfo.md#associatedframeinfos). CoreWebView2FrameInfo objects obtained via [CoreWebView2.ProcessFailed](corewebview2.md#processfailed) will always have a `null` ParentFrameInfo. This property is also `null` for the top most document in the [CoreWebView2](corewebview2.md) which has no parent frame.
[Source](#source) | The URI of the document in the frame.

## Properties

### FrameId

> readonly  uint32_t FrameId

The unique identifier of the frame associated with the current CoreWebView2FrameInfo. It's the same kind of ID as with the [CoreWebView2.FrameId](corewebview2.md#frameid) and [CoreWebView2Frame.FrameId](corewebview2frame.md#frameid). FrameId will only be populated when obtained calling [CoreWebView2ProcessInfo.AssociatedFrameInfos](corewebview2processinfo.md#associatedframeinfos). CoreWebView2FrameInfo objects obtained via [CoreWebView2.ProcessFailed](corewebview2.md#processfailed) will always have an invalid frame Id `0`.
FrameId could be out of date as it's a snapshot.

### FrameKind

> readonly  [CoreWebView2FrameKind](corewebview2framekind.md) FrameKind

Gets the kind of the frame. FrameKind will only be populated when obtained calling [CoreWebView2ProcessInfo.AssociatedFrameInfos](corewebview2processinfo.md#associatedframeinfos). CoreWebView2FrameInfo objects obtained via [CoreWebView2.ProcessFailed](corewebview2.md#processfailed) will always have the default value [CoreWebView2FrameKind.Other](corewebview2framekind.md).
FrameKind could be out of date as it's a snapshot.

### Name

> readonly  string Name

Gets the name attribute of the frame, as in `<iframe name="frame-name" ...>`.
The returned string is empty when the frame has no name attribute.

### ParentFrameInfo

> readonly  CoreWebView2FrameInfo ParentFrameInfo

This frame's parent frame's CoreWebView2FrameInfo. ParentFrameInfo will only be populated when obtained via calling [CoreWebView2ProcessInfo.AssociatedFrameInfos](corewebview2processinfo.md#associatedframeinfos). CoreWebView2FrameInfo objects obtained via [CoreWebView2.ProcessFailed](corewebview2.md#processfailed) will always have a `null` ParentFrameInfo. This property is also `null` for the top most document in the [CoreWebView2](corewebview2.md) which has no parent frame.
ParentFrameInfo could be out of date as it's a snapshot.

### Source

> readonly  string Source

The URI of the document in the frame.




