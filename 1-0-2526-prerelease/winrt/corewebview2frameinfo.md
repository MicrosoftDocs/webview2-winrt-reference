---
description: Provides a set of properties for a frame in the CoreWebView2.
title: CoreWebView2FrameInfo
ms.date: 04/22/2024
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2FrameInfo
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- Microsoft.Web.WebView2.Core.CoreWebView2FrameInfo
- Microsoft.Web.WebView2.Core.CoreWebView2FrameInfo.FrameId
- Microsoft.Web.WebView2.Core.CoreWebView2FrameInfo.FrameKind
- Microsoft.Web.WebView2.Core.CoreWebView2FrameInfo.Name
- Microsoft.Web.WebView2.Core.CoreWebView2FrameInfo.ParentFrameInfo
- Microsoft.Web.WebView2.Core.CoreWebView2FrameInfo.Source
- Microsoft.Web.WebView2.Core.CoreWebView2FrameInfo.get_FrameId
- Microsoft.Web.WebView2.Core.CoreWebView2FrameInfo.get_FrameKind
- Microsoft.Web.WebView2.Core.CoreWebView2FrameInfo.get_Name
- Microsoft.Web.WebView2.Core.CoreWebView2FrameInfo.get_ParentFrameInfo
- Microsoft.Web.WebView2.Core.CoreWebView2FrameInfo.get_Source
---

# CoreWebView2FrameInfo Class



Provides a set of properties for a frame in the [CoreWebView2](corewebview2.md).

## Summary

Members|Description
--|--
[FrameId](#frameid) | The unique identifier of the frame associated with the current CoreWebView2FrameInfo. It's the same kind of ID as with the [CoreWebView2.FrameId](corewebview2.md#frameid) and [CoreWebView2Frame.FrameId](corewebview2frame.md#frameid). FrameId will only be populated when obtained calling [CoreWebView2ProcessExtendedInfo.AssociatedFrameInfos](corewebview2processextendedinfo.md#associatedframeinfos). CoreWebView2FrameInfo objects obtained via [CoreWebView2.ProcessFailed](corewebview2.md#processfailed) will always have an invalid frame Id `0`.
[FrameKind](#framekind) | Gets the kind of the frame. FrameKind will only be populated when obtained calling [CoreWebView2ProcessExtendedInfo.AssociatedFrameInfos](corewebview2processextendedinfo.md#associatedframeinfos). [CoreWebView2ProcessExtendedInfo.CoreWebView2FrameInfo](corewebview2processextendedinfo.md#corewebview2frameinfo) objects obtained via [CoreWebView2.ProcessFailed](corewebview2.md#processfailed) will always have the default value [CoreWebView2FrameKind](corewebview2framekind.md).Other.
[Name](#name) | Gets the value of frame's `window.name` property. The default value equals to frame html tag declaring it, as in `<iframe name="frame-name" ...>`.
[ParentFrameInfo](#parentframeinfo) | This parent frame's CoreWebView2FrameInfo. ParentFrameInfo will only be populated when obtained via calling [CoreWebView2ProcessExtendedInfo.AssociatedFrameInfos](corewebview2processextendedinfo.md#associatedframeinfos). CoreWebView2FrameInfo objects obtained via [CoreWebView2.ProcessFailed](corewebview2.md#processfailed) will always have a `null` ParentFrameInfo. This property is also `null` for the top most document in the [CoreWebView2](corewebview2.md) which has no parent frame.
[Source](#source) | The URI of the document in the frame.

## Properties

### FrameId

> readonly  uint32_t FrameId

The unique identifier of the frame associated with the current CoreWebView2FrameInfo. It's the same kind of ID as with the [CoreWebView2.FrameId](corewebview2.md#frameid) and [CoreWebView2Frame.FrameId](corewebview2frame.md#frameid). FrameId will only be populated when obtained calling [CoreWebView2ProcessExtendedInfo.AssociatedFrameInfos](corewebview2processextendedinfo.md#associatedframeinfos). CoreWebView2FrameInfo objects obtained via [CoreWebView2.ProcessFailed](corewebview2.md#processfailed) will always have an invalid frame Id `0`.
FrameId could be out of date as it's a snapshot. If there's [CoreWebView2](corewebview2.md) created or destroyed or [CoreWebView2.FrameCreated](corewebview2.md#framecreated) event or [CoreWebView2Frame.Destroyed](corewebview2frame.md#destroyed) event after the asynchronous call [CoreWebView2Environment.GetProcessExtendedInfosAsync](corewebview2environment.md#getprocessextendedinfosasync) starts, you may want to call the asynchronous method again to get the updated CoreWebView2FrameInfo s.

### FrameKind

> readonly  [CoreWebView2FrameKind](corewebview2framekind.md) FrameKind

Gets the kind of the frame. FrameKind will only be populated when obtained calling [CoreWebView2ProcessExtendedInfo.AssociatedFrameInfos](corewebview2processextendedinfo.md#associatedframeinfos). [CoreWebView2ProcessExtendedInfo.CoreWebView2FrameInfo](corewebview2processextendedinfo.md#corewebview2frameinfo) objects obtained via [CoreWebView2.ProcessFailed](corewebview2.md#processfailed) will always have the default value [CoreWebView2FrameKind](corewebview2framekind.md).Other.
FrameKind could be out of date as it's a snapshot.

### Name

> readonly  string Name

Gets the value of frame's `window.name` property. The default value equals to frame html tag declaring it, as in `<iframe name="frame-name" ...>`.
The returned string is empty when the frame has no name attribute and no assigned value for window.name.

### ParentFrameInfo

> readonly  CoreWebView2FrameInfo ParentFrameInfo

This parent frame's CoreWebView2FrameInfo. ParentFrameInfo will only be populated when obtained via calling [CoreWebView2ProcessExtendedInfo.AssociatedFrameInfos](corewebview2processextendedinfo.md#associatedframeinfos). CoreWebView2FrameInfo objects obtained via [CoreWebView2.ProcessFailed](corewebview2.md#processfailed) will always have a `null` ParentFrameInfo. This property is also `null` for the top most document in the [CoreWebView2](corewebview2.md) which has no parent frame.
ParentFrameInfo could be out of date as it's a snapshot.

### Source

> readonly  string Source

The URI of the document in the frame.






## Referenced by

- [CoreWebView2NewWindowRequestedEventArgs](corewebview2newwindowrequestedeventargs.md)
