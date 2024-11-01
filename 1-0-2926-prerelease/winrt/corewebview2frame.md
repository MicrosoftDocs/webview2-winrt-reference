---
title: CoreWebView2Frame
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/01/2024
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2Frame
---

# runtimeClass CoreWebView2Frame



## Summary

Members|Description
--|--
[FrameId](#frameid) | 
[Name](#name) | 
[UseOverrideTimerWakeInterval](#useoverridetimerwakeinterval) | 
[ExecuteScriptAsync](#executescriptasync) | 
[IsDestroyed](#isdestroyed) | 
[PostSharedBufferToScript](#postsharedbuffertoscript) | 
[PostWebMessageAsJson](#postwebmessageasjson) | 
[PostWebMessageAsString](#postwebmessageasstring) | 
[RemoveHostObjectFromScript](#removehostobjectfromscript) | 
[ContentLoading](#contentloading) | 
[DOMContentLoaded](#domcontentloaded) | 
[Destroyed](#destroyed) | 
[NameChanged](#namechanged) | 
[NavigationCompleted](#navigationcompleted) | 
[NavigationStarting](#navigationstarting) | 
[PermissionRequested](#permissionrequested) | 
[ScreenCaptureStarting](#screencapturestarting) | 
[WebMessageReceived](#webmessagereceived) | 

## Properties

### FrameId

> readonly  uint32_t FrameId

### Name

> readonly  string Name

### UseOverrideTimerWakeInterval

>  bool UseOverrideTimerWakeInterval



## Methods

### ExecuteScriptAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;string&gt; ExecuteScriptAsync(string operation)



### IsDestroyed

> int IsDestroyed()



### PostSharedBufferToScript

> void PostSharedBufferToScript([CoreWebView2SharedBuffer](corewebview2sharedbuffer.md) sharedBuffer, [CoreWebView2SharedBufferAccess](corewebview2sharedbufferaccess.md) access, string additionalDataAsJson)



### PostWebMessageAsJson

> void PostWebMessageAsJson(string webMessageAsJson)



### PostWebMessageAsString

> void PostWebMessageAsString(string webMessageAsString)



### RemoveHostObjectFromScript

> void RemoveHostObjectFromScript(string name)




## Events

### ContentLoading

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2Frame](corewebview2frame.md), [CoreWebView2ContentLoadingEventArgs](corewebview2contentloadingeventargs.md)&gt;

### DOMContentLoaded

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2Frame](corewebview2frame.md), [CoreWebView2DOMContentLoadedEventArgs](corewebview2domcontentloadedeventargs.md)&gt;

### Destroyed

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2Frame](corewebview2frame.md), Object&gt;

### NameChanged

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2Frame](corewebview2frame.md), Object&gt;

### NavigationCompleted

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2Frame](corewebview2frame.md), [CoreWebView2NavigationCompletedEventArgs](corewebview2navigationcompletedeventargs.md)&gt;

### NavigationStarting

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2Frame](corewebview2frame.md), [CoreWebView2NavigationStartingEventArgs](corewebview2navigationstartingeventargs.md)&gt;

### PermissionRequested

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2Frame](corewebview2frame.md), [CoreWebView2PermissionRequestedEventArgs](corewebview2permissionrequestedeventargs.md)&gt;

### ScreenCaptureStarting

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2Frame](corewebview2frame.md), [CoreWebView2ScreenCaptureStartingEventArgs](corewebview2screencapturestartingeventargs.md)&gt;

### WebMessageReceived

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2Frame](corewebview2frame.md), [CoreWebView2WebMessageReceivedEventArgs](corewebview2webmessagereceivedeventargs.md)&gt;



## Referenced by

- [CoreWebView2FrameCreatedEventArgs](corewebview2framecreatedeventargs.md)
