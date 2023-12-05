---
description: Event args for the CoreWebView2.PermissionRequested event.
title: CoreWebView2PermissionRequestedEventArgs
ms.date: 12/11/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2PermissionRequestedEventArgs
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- Microsoft.Web.WebView2.Core.CoreWebView2PermissionRequestedEventArgs
- Microsoft.Web.WebView2.Core.CoreWebView2PermissionRequestedEventArgs.Handled
- Microsoft.Web.WebView2.Core.CoreWebView2PermissionRequestedEventArgs.IsUserInitiated
- Microsoft.Web.WebView2.Core.CoreWebView2PermissionRequestedEventArgs.PermissionKind
- Microsoft.Web.WebView2.Core.CoreWebView2PermissionRequestedEventArgs.SavesInProfile
- Microsoft.Web.WebView2.Core.CoreWebView2PermissionRequestedEventArgs.State
- Microsoft.Web.WebView2.Core.CoreWebView2PermissionRequestedEventArgs.Uri
- Microsoft.Web.WebView2.Core.CoreWebView2PermissionRequestedEventArgs.GetDeferral
- Microsoft.Web.WebView2.Core.CoreWebView2PermissionRequestedEventArgs.get_Handled
- Microsoft.Web.WebView2.Core.CoreWebView2PermissionRequestedEventArgs.get_IsUserInitiated
- Microsoft.Web.WebView2.Core.CoreWebView2PermissionRequestedEventArgs.get_PermissionKind
- Microsoft.Web.WebView2.Core.CoreWebView2PermissionRequestedEventArgs.get_SavesInProfile
- Microsoft.Web.WebView2.Core.CoreWebView2PermissionRequestedEventArgs.get_State
- Microsoft.Web.WebView2.Core.CoreWebView2PermissionRequestedEventArgs.get_Uri
- Microsoft.Web.WebView2.Core.CoreWebView2PermissionRequestedEventArgs.put_Handled
- Microsoft.Web.WebView2.Core.CoreWebView2PermissionRequestedEventArgs.put_SavesInProfile
- Microsoft.Web.WebView2.Core.CoreWebView2PermissionRequestedEventArgs.put_State
---

# CoreWebView2PermissionRequestedEventArgs Class



Event args for the [CoreWebView2.PermissionRequested](corewebview2.md#permissionrequested) event.

## Summary

Members|Description
--|--
[Handled](#handled) | The host may set this flag to `TRUE` to prevent the `PermissionRequested` event from firing on the `CoreWebView2` as well.
[IsUserInitiated](#isuserinitiated) | `true` when the permission request was initiated through a user gesture such as clicking an anchor tag with target.
[PermissionKind](#permissionkind) | Gets the kind of the permission that is requested.
[SavesInProfile](#savesinprofile) | Set the `SavesInProfile` property to `FALSE` to not persist the state beyond the current request, and to continue to receive `PermissionRequested` events for this origin and permission kind.
[State](#state) | Gets or sets the status of a permission request. For example, whether the request is granted.
[Uri](#uri) | Gets the origin of the web content that requests the permission.
[GetDeferral](#getdeferral) | Gets a Deferral object.

## Properties

### Handled

>  bool Handled

The host may set this flag to `TRUE` to prevent the `PermissionRequested` event from firing on the `CoreWebView2` as well.
By default, both the `PermissionRequested` on the `CoreWebView2Frame` and `CoreWebView2` will be fired.

### IsUserInitiated

> readonly  bool IsUserInitiated

`true` when the permission request was initiated through a user gesture such as clicking an anchor tag with target.
Being initiated through a user gesture does not mean that user intended to access the associated resource.

### PermissionKind

> readonly  [CoreWebView2PermissionKind](corewebview2permissionkind.md) PermissionKind

Gets the kind of the permission that is requested.

### SavesInProfile

>  bool SavesInProfile

Set the `SavesInProfile` property to `FALSE` to not persist the state beyond the current request, and to continue to receive `PermissionRequested` events for this origin and permission kind.
The permission state set from the `PermissionRequested`  event is saved in the profile by default; it is persisted across sessions and becomes the new default behavior for future `PermissionRequested`  events. Browser heuristics can affect whether the event continues to be raised when the state is persisted.

### State

>  [CoreWebView2PermissionState](corewebview2permissionstate.md) State

Gets or sets the status of a permission request. For example, whether the request is granted.
The default value is [CoreWebView2PermissionState](corewebview2permissionstate.md).Default.

### Uri

> readonly  string Uri

Gets the origin of the web content that requests the permission.



## Methods

### GetDeferral

> [Deferral](/uwp/api/Windows.Foundation.Deferral) GetDeferral()

Gets a Deferral object.
Use the deferral object to make the permission decision at a later time. The deferral only applies to the current request, and does not prevent the `PermissionRequested` event from getting raised for new requests. However, for some permission kinds the WebView will avoid creating a new request if there is a pending request of the same kind.






## Referenced by

- [CoreWebView2](corewebview2.md)
- [CoreWebView2Frame](corewebview2frame.md)
