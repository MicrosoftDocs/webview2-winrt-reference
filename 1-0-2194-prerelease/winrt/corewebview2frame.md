---
description: 
title: CoreWebView2Frame
ms.date: 11/06/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2Frame
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- Microsoft.Web.WebView2.Core.CoreWebView2Frame
- Microsoft.Web.WebView2.Core.CoreWebView2Frame.FrameId
- Microsoft.Web.WebView2.Core.CoreWebView2Frame.Name
- Microsoft.Web.WebView2.Core.CoreWebView2Frame.ExecuteScriptAsync
- Microsoft.Web.WebView2.Core.CoreWebView2Frame.IsDestroyed
- Microsoft.Web.WebView2.Core.CoreWebView2Frame.PostSharedBufferToScript
- Microsoft.Web.WebView2.Core.CoreWebView2Frame.PostWebMessageAsJson
- Microsoft.Web.WebView2.Core.CoreWebView2Frame.PostWebMessageAsString
- Microsoft.Web.WebView2.Core.CoreWebView2Frame.RemoveHostObjectFromScript
- Microsoft.Web.WebView2.Core.CoreWebView2Frame.add_ContentLoading
- Microsoft.Web.WebView2.Core.CoreWebView2Frame.add_DOMContentLoaded
- Microsoft.Web.WebView2.Core.CoreWebView2Frame.add_Destroyed
- Microsoft.Web.WebView2.Core.CoreWebView2Frame.add_NameChanged
- Microsoft.Web.WebView2.Core.CoreWebView2Frame.add_NavigationCompleted
- Microsoft.Web.WebView2.Core.CoreWebView2Frame.add_NavigationStarting
- Microsoft.Web.WebView2.Core.CoreWebView2Frame.add_PermissionRequested
- Microsoft.Web.WebView2.Core.CoreWebView2Frame.add_WebMessageReceived
- Microsoft.Web.WebView2.Core.CoreWebView2Frame.get_FrameId
- Microsoft.Web.WebView2.Core.CoreWebView2Frame.get_Name
- Microsoft.Web.WebView2.Core.CoreWebView2Frame.remove_ContentLoading
- Microsoft.Web.WebView2.Core.CoreWebView2Frame.remove_DOMContentLoaded
- Microsoft.Web.WebView2.Core.CoreWebView2Frame.remove_Destroyed
- Microsoft.Web.WebView2.Core.CoreWebView2Frame.remove_NameChanged
- Microsoft.Web.WebView2.Core.CoreWebView2Frame.remove_NavigationCompleted
- Microsoft.Web.WebView2.Core.CoreWebView2Frame.remove_NavigationStarting
- Microsoft.Web.WebView2.Core.CoreWebView2Frame.remove_PermissionRequested
- Microsoft.Web.WebView2.Core.CoreWebView2Frame.remove_WebMessageReceived
- Microsoft.Web.WebView2.Core.CoreWebView2Frame.ContentLoading
- Microsoft.Web.WebView2.Core.CoreWebView2Frame.DOMContentLoaded
- Microsoft.Web.WebView2.Core.CoreWebView2Frame.Destroyed
- Microsoft.Web.WebView2.Core.CoreWebView2Frame.NameChanged
- Microsoft.Web.WebView2.Core.CoreWebView2Frame.NavigationCompleted
- Microsoft.Web.WebView2.Core.CoreWebView2Frame.NavigationStarting
- Microsoft.Web.WebView2.Core.CoreWebView2Frame.PermissionRequested
- Microsoft.Web.WebView2.Core.CoreWebView2Frame.WebMessageReceived
---

# CoreWebView2Frame Class



## Summary

Members|Description
--|--
[FrameId](#frameid) | 
[Name](#name) | 
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
[WebMessageReceived](#webmessagereceived) | 

## Properties

### FrameId

> readonly  uint32_t FrameId

### Name

> readonly  string Name



## Methods

### ExecuteScriptAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;string&gt; ExecuteScriptAsync(string javaScript)



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

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2Frame, [CoreWebView2ContentLoadingEventArgs](corewebview2contentloadingeventargs.md)&gt;

### DOMContentLoaded

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2Frame, [CoreWebView2DOMContentLoadedEventArgs](corewebview2domcontentloadedeventargs.md)&gt;

### Destroyed

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2Frame, Object&gt;

### NameChanged

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2Frame, Object&gt;

### NavigationCompleted

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2Frame, [CoreWebView2NavigationCompletedEventArgs](corewebview2navigationcompletedeventargs.md)&gt;

### NavigationStarting

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2Frame, [CoreWebView2NavigationStartingEventArgs](corewebview2navigationstartingeventargs.md)&gt;

### PermissionRequested

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2Frame, [CoreWebView2PermissionRequestedEventArgs](corewebview2permissionrequestedeventargs.md)&gt;

### WebMessageReceived

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2Frame, [CoreWebView2WebMessageReceivedEventArgs](corewebview2webmessagereceivedeventargs.md)&gt;



## Referenced by

- [CoreWebView2FrameCreatedEventArgs](corewebview2framecreatedeventargs.md)
