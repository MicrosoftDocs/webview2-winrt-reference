---
description: Used to manage profile options that created by CoreWebView2Environment.CreateCoreWebView2ControllerOptions.
title: CoreWebView2ControllerOptions
ms.date: 09/06/2022
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ControllerOptions
---

# CoreWebView2ControllerOptions Class



Used to manage profile options that created by [CoreWebView2Environment.CreateCoreWebView2ControllerOptions](corewebview2environment.md#createcorewebview2controlleroptions).

## Summary

Members|Description
--|--
[IsInPrivateModeEnabled](#isinprivatemodeenabled) | Manage the controller's InPrivate mode.
[ProfileName](#profilename) | Manage the name of the controller's profile.

## Properties

### IsInPrivateModeEnabled

>  bool IsInPrivateModeEnabled

Manage the controller's InPrivate mode.

### ProfileName

>  string ProfileName

Manage the name of the controller's profile.
The `ProfileName` property is to specify a profile name, which is only allowed to contain the following ASCII characters. It has a maximum length of 64 characters excluding the null-terminator. It is ASCII case insensitive.

* alphabet characters: a-z and A-Z
* digit characters: 0-9
* and '#', '[]()', '', '(', ')', '+', '-', '_', '~', '.', ' ' (space).

Note: the text must not end with a period '.' or ' ' (space). And, although upper-case letters are allowed, they're treated just as lower-case counterparts because the profile name will be mapped to the real profile directory path on disk and Windows file system handles path names in a case-insensitive way.






## Referenced by

- [CoreWebView2Environment](corewebview2environment.md)
