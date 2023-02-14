---
description: Used to manage profile options that created by CoreWebView2Environment.CreateCoreWebView2ControllerOptions.
title: CoreWebView2ControllerOptions
ms.date: 02/14/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ControllerOptions
---

# CoreWebView2ControllerOptions Class



Used to manage profile options that created by [CoreWebView2Environment.CreateCoreWebView2ControllerOptions](corewebview2environment.md#createcorewebview2controlleroptions).

## Summary

Members|Description
--|--
[IsInPrivateModeEnabled](#isinprivatemodeenabled) | Manage the controller's InPrivate mode.
[LocaleRegion](#localeregion) | Manages the value of the controller's locale region.
[ProfileName](#profilename) | Manage the name of the controller's profile.
[ScriptLocale](#scriptlocale) | Manages the value of the controller's script locale.

## Properties

### IsInPrivateModeEnabled

>  bool IsInPrivateModeEnabled

Manage the controller's InPrivate mode.

### LocaleRegion

>  string LocaleRegion

Manages the value of the controller's locale region.
The `LocaleRegion` property is to specify the default locale region. It sets the default locale for all Intl JavaScript APIs and other JavaScript APIs that depend on it, namely `Intl.DateTimeFormat()` which affects string formatting like in the time/date formats.The intended locale value is in the format of BCP 47 Language Tags. More information can be found from [IETF BCP47](https://www.ietf.org/rfc/bcp/bcp47.html).
The default value for LocaleRegion will be depend on the WebView2 language and OS region. If the language portions of the WebView2 language and OS region match, then it will use the OS region. Otherwise, it will use the WebView2 language.
| **OS Region** | **WebView2 Language** | **Default WebView2 LocaleRegion** |
|-----------|-------------------|-------------------------------|
| en-GB     | en-US             | en-GB                         |
| es-MX     | en-US             | en-US                         |
| en-US     | en-GB             | en-US                         |
You can set the LocaleRegion to the empty string to get the default LocaleRegion value.
Use OS specific APIs to determine the OS region to use with this property if you always want to match with the OS
region. For example:
```csharp
CultureInfo cultureInfo = Thread.CurrentThread.CurrentCulture;
return cultureInfo.Name
```

### ProfileName

>  string ProfileName

Manage the name of the controller's profile.
The `ProfileName` property is to specify a profile name, which is only allowed to contain the following ASCII characters. It has a maximum length of 64 characters excluding the null-terminator. It is ASCII case insensitive.

* alphabet characters: a-z and A-Z
* digit characters: 0-9
* and '#', '@', '', '(', ')', '+', '-', '_', '~', '.', ' ' (space).

Note: the text must not end with a period '.' or ' ' (space). And, although upper-case letters are allowed, they're treated just as lower-case counterparts because the profile name will be mapped to the real profile directory path on disk and Windows file system handles path names in a case-insensitive way.

### ScriptLocale

>  string ScriptLocale

Manages the value of the controller's script locale.
The `ScriptLocale` property is to specify the default script locale. It sets the default locale for all Intl JavaScript APIs and other JavaScript APIs that depend on it, namely `Intl.DateTimeFormat()` which affects string formatting like in the time/date formats.The intended locale value is in the format of BCP 47 Language Tags. More information can be found from [IETF BCP47](https://www.ietf.org/rfc/bcp/bcp47.html).
The default value for ScriptLocale will be depend on the WebView2 language and OS region. If the language portions of the WebView2 language and OS region match, then it will use the OS region. Otherwise, it will use the WebView2 language.
| **OS Region** | **WebView2 Language** | **Default WebView2 ScriptLocale** |
|-----------|-------------------|-------------------------------|
| en-GB     | en-US             | en-GB                         |
| es-MX     | en-US             | en-US                         |
| en-US     | en-GB             | en-US                         |
You can set the ScriptLocale to the empty string to get the default ScriptLocale value.
Use OS specific APIs to determine the OS region to use with this property if you always want to match with the OS
region. For example:
```csharp
CultureInfo cultureInfo = Thread.CurrentThread.CurrentCulture;
return cultureInfo.Name
```






## Referenced by

- [CoreWebView2Environment](corewebview2environment.md)
