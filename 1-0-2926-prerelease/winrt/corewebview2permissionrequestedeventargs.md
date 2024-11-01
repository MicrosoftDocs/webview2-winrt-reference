---
title: CoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/01/2024
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2PermissionRequestedEventArgs
---

# runtimeClass CoreWebView2PermissionRequestedEventArgs



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
