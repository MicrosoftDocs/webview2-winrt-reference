---
description: 
title: CoreWebView2PermissionRequestedEventArgs
ms.date: 10/16/2023
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



## Summary

Members|Description
--|--
[Handled](#handled) | 
[IsUserInitiated](#isuserinitiated) | 
[PermissionKind](#permissionkind) | 
[SavesInProfile](#savesinprofile) | 
[State](#state) | 
[Uri](#uri) | 
[GetDeferral](#getdeferral) | 

## Properties

### Handled

>  bool Handled

### IsUserInitiated

> readonly  bool IsUserInitiated

### PermissionKind

> readonly  [CoreWebView2PermissionKind](corewebview2permissionkind.md) PermissionKind

### SavesInProfile

>  bool SavesInProfile

### State

>  [CoreWebView2PermissionState](corewebview2permissionstate.md) State

### Uri

> readonly  string Uri



## Methods

### GetDeferral

> [Deferral](/uwp/api/Windows.Foundation.Deferral) GetDeferral()






## Referenced by

- [CoreWebView2](corewebview2.md)
- [CoreWebView2Frame](corewebview2frame.md)
