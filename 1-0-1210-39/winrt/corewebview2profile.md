---
description: Multiple profiles can be created under a single user data directory but with separated cookies, user preference settings, and various data storage etc.. If the CoreWebView2 was created with a CoreWebView2ControllerOptions, the CoreWebView2Profile will match those specified options. Otherwise if this CoreWebView2 was created without a CoreWebView2ControllerOptions, then this will be the default CoreWebView2Profile for the corresponding CoreWebView2Environment.
title: CoreWebView2Profile
ms.date: 05/17/2022
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2Profile
---

# CoreWebView2Profile Class



Multiple profiles can be created under a single user data directory but with separated cookies, user preference settings, and various data storage etc.. If the CoreWebView2 was created with a [CoreWebView2ControllerOptions](corewebview2controlleroptions.md), the CoreWebView2Profile will match those specified options. Otherwise if this CoreWebView2 was created without a [CoreWebView2ControllerOptions](corewebview2controlleroptions.md), then this will be the default CoreWebView2Profile for the corresponding CoreWebView2Environment.

## Summary

Members|Description
--|--
[DefaultDownloadFolderPath](#defaultdownloadfolderpath) | The default download folder path.
[IsInPrivateModeEnabled](#isinprivatemodeenabled) | InPrivate mode is enabled or not.
[PreferredColorScheme](#preferredcolorscheme) | The PreferredColorScheme property sets the overall color scheme of the WebView2s associated with this profile.
[ProfileName](#profilename) | The name of the profile.
[ProfilePath](#profilepath) | Full path of the profile directory.

## Properties

### DefaultDownloadFolderPath

>  string DefaultDownloadFolderPath

The default download folder path.
The default value is the system default download folder path for the user. The default download folder path is persisted in the user data folder across sessions. The value should be an absolute path to a folder that the user and application can write to. Throws an exception if the value is invalid, and the default download path is not changed. Otherwise the path is changed immediately. If the directory does not yet exist, it is created at the time of the next download. If the host application does not have permission to create the directory, then the user is prompted to provide a new path through the Save As dialog. The user can override the default download folder path for a given download by choosing a different path in the Save As dialog.

### IsInPrivateModeEnabled

> readonly  bool IsInPrivateModeEnabled

InPrivate mode is enabled or not.

### PreferredColorScheme

>  [CoreWebView2PreferredColorScheme](corewebview2preferredcolorscheme.md) PreferredColorScheme

The PreferredColorScheme property sets the overall color scheme of the WebView2s associated with this profile.
This sets the color scheme for WebView2 UI like dialogs, prompts, and menus by setting the media feature `prefers-color-scheme`.
The default value for this is [CoreWebView2PreferredColorScheme](corewebview2preferredcolorscheme.md).Auto, which will follow whatever color scheme the OS is currently set to.

### ProfileName

> readonly  string ProfileName

The name of the profile.

### ProfilePath

> readonly  string ProfilePath

Full path of the profile directory.






## Referenced by

- [CoreWebView2](corewebview2.md)
