---
description: Event args for the CoreWebView2.PermissionRequested event.
title: CoreWebView2PermissionRequestedEventArgs
ms.date: 08/16/2021
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2PermissionRequestedEventArgs
---

# runtimeclass CoreWebView2PermissionRequestedEventArgs



Event args for the [CoreWebView2.PermissionRequested](corewebview2.md#permissionrequested) event.

## Summary

Members|Description
--|--
[IsUserInitiated](#isuserinitiated) | `true` when the permission request was initiated through a user gesture such as clicking an anchor tag with target.
[PermissionKind](#permissionkind) | Gets the kind of the permission that is requested.
[State](#state) | Gets or sets the status of a permission request. For example, whether the request is granted.
[Uri](#uri) | Gets the origin of the web content that requests the permission.
[GetDeferral](#getdeferral) | Gets a Deferral object.

## Properties

### IsUserInitiated

> readonly  bool IsUserInitiated

`true` when the permission request was initiated through a user gesture such as clicking an anchor tag with target.

Being initiated through a user gesture does not mean that user intended to access the associated resource.

### PermissionKind

> readonly  [CoreWebView2PermissionKind](corewebview2permissionkind.md) PermissionKind

Gets the kind of the permission that is requested.

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

Use the deferral object to make the permission decision at a later time.






## Referenced by

- [CoreWebView2](corewebview2.md)
