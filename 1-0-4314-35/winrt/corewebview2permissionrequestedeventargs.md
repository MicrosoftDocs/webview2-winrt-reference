---
description: Event args for the CoreWebView2.PermissionRequested event.
title: CoreWebView2PermissionRequestedEventArgs
ms.date: 10-29-2026
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2PermissionRequestedEventArgs
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2PermissionRequestedEventArgs
- CoreWebView2PermissionRequestedEventArgs.Handled
- CoreWebView2PermissionRequestedEventArgs.IsUserInitiated
- CoreWebView2PermissionRequestedEventArgs.PermissionKind
- CoreWebView2PermissionRequestedEventArgs.SavesInProfile
- CoreWebView2PermissionRequestedEventArgs.State
- CoreWebView2PermissionRequestedEventArgs.Uri
- CoreWebView2PermissionRequestedEventArgs.GetDeferral
---

# CoreWebView2PermissionRequestedEventArgs Class



Event args for the [CoreWebView2.PermissionRequested](corewebview2.md#permissionrequested) event.

## Summary

Members|Description
--|--
[Handled](#handled) | The host may set this flag to `true` to prevent the [CoreWebView2.PermissionRequested](corewebview2.md#permissionrequested) event from firing on the [CoreWebView2](corewebview2.md) as well.
[IsUserInitiated](#isuserinitiated) | `true` when the permission request was initiated through a user gesture such as clicking an anchor tag with target.
[PermissionKind](#permissionkind) | Gets the kind of the permission that is requested.
[SavesInProfile](#savesinprofile) | Set the [CoreWebView2PermissionRequestedEventArgs.SavesInProfile](corewebview2permissionrequestedeventargs.md#savesinprofile) property to `false` to not persist the state beyond the current request, and to continue to receive [CoreWebView2.PermissionRequested](corewebview2.md#permissionrequested) events for this origin and permission kind.
[State](#state) | Gets or sets the status of a permission request.
[Uri](#uri) | Gets the origin of the web content that requests the permission.
[GetDeferral](#getdeferral) | Gets a [Deferral](/uwp/api/windows.foundation.deferral) object.

## Properties

### Handled

>  bool Handled

The host may set this flag to `true` to prevent the [CoreWebView2.PermissionRequested](corewebview2.md#permissionrequested) event from firing on the [CoreWebView2](corewebview2.md) as well.

By default, both the [CoreWebView2Frame.PermissionRequested](corewebview2frame.md#permissionrequested) event on the [CoreWebView2Frame](corewebview2frame.md) and the [CoreWebView2.PermissionRequested](corewebview2.md#permissionrequested) event on the [CoreWebView2](corewebview2.md) will be fired, with the [CoreWebView2Frame](corewebview2frame.md) event handlers invoked first. The host may set this flag to `true` within the [CoreWebView2Frame.PermissionRequested](corewebview2frame.md#permissionrequested) event handlers to prevent the remaining [CoreWebView2.PermissionRequested](corewebview2.md#permissionrequested) event handlers from being invoked.

If a deferral is taken on the event args, then you must synchronously set [CoreWebView2PermissionRequestedEventArgs.Handled](corewebview2permissionrequestedeventargs.md#handled) to `true` prior to taking your deferral to prevent the [CoreWebView2](corewebview2.md)'s event handlers from being invoked.

### IsUserInitiated

> readonly  bool IsUserInitiated

`true` when the permission request was initiated through a user gesture such as clicking an anchor tag with target.

Being initiated through a user gesture does not mean that user intended to access the associated resource.

### PermissionKind

> readonly  [CoreWebView2PermissionKind](corewebview2permissionkind.md) PermissionKind

Gets the kind of the permission that is requested.

### SavesInProfile

>  bool SavesInProfile

Set the [CoreWebView2PermissionRequestedEventArgs.SavesInProfile](corewebview2permissionrequestedeventargs.md#savesinprofile) property to `false` to not persist the state beyond the current request, and to continue to receive [CoreWebView2.PermissionRequested](corewebview2.md#permissionrequested) events for this origin and permission kind.

The permission state set from the [CoreWebView2.PermissionRequested](corewebview2.md#permissionrequested) event is saved in the profile by default; it is persisted across sessions and becomes the new default behavior for future [CoreWebView2.PermissionRequested](corewebview2.md#permissionrequested) events. Browser heuristics can affect whether the event continues to be raised when the state is persisted.

### State

>  [CoreWebView2PermissionState](corewebview2permissionstate.md) State

Gets or sets the status of a permission request.
For example, whether the request is granted.

The default value is [CoreWebView2PermissionState](corewebview2permissionstate.md).Default.

### Uri

> readonly  string Uri

Gets the origin of the web content that requests the permission.



## Methods

### GetDeferral

> [Deferral](/uwp/api/Windows.Foundation.Deferral) GetDeferral()

Gets a [Deferral](/uwp/api/windows.foundation.deferral) object.

Use the deferral object to make the permission decision at a later time. The deferral only applies to the current request, and does not prevent the [CoreWebView2.PermissionRequested](corewebview2.md#permissionrequested) event from getting raised for new requests. However, for some permission kinds the WebView will avoid creating a new request if there is a pending request of the same kind.






## Referenced by

- [CoreWebView2](corewebview2.md)
- [CoreWebView2Frame](corewebview2frame.md)
