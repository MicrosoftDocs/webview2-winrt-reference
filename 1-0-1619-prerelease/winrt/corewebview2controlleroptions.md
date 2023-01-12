---
description: Used to manage profile options that created by CoreWebView2Environment.CreateCoreWebView2ControllerOptions.
title: CoreWebView2ControllerOptions
ms.date: 01/17/2023
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

## Properties

### IsInPrivateModeEnabled

>  bool IsInPrivateModeEnabled

Manage the controller's InPrivate mode.

### LocaleRegion

>  string LocaleRegion

Manages the value of the controller's locale region.
The `LocaleRegion` property is to specify the default locale region, as it applies to the browser UI such as in the time/date formats. The intended locale value is in the format of `language[-country]` where `language` is the 2-letter code from [ISO 639](https://www.iso.org/iso-639-language-codes.html) and `country` is the 2-letter code from [ISO 3166](https://www.iso.org/standard/72482.html).
Validation is done on the downstream V8 engine to match on the closest locale from the passed in locale region value. For example, passing in "en_gb" will reflect the "en-GB" locale in V8. If V8 cannot find any matching locale on the input value, it will default to the display language as the locale.
The LocaleRegion can be reset back to the Limited default option by passing in an empty string.
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






## Referenced by

- [CoreWebView2Environment](corewebview2environment.md)
