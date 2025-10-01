---
description: Used to manage profile options that created by CoreWebView2Environment.CreateCoreWebView2ControllerOptions.
title: CoreWebView2ControllerOptions
ms.date: 10/01/2025
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ControllerOptions
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2ControllerOptions
- CoreWebView2ControllerOptions.AllowHostInputProcessing
- CoreWebView2ControllerOptions.DefaultBackgroundColor
- CoreWebView2ControllerOptions.IsInPrivateModeEnabled
- CoreWebView2ControllerOptions.ProfileName
- CoreWebView2ControllerOptions.ScriptLocale
---

# CoreWebView2ControllerOptions Class



Used to manage profile options that created by [CoreWebView2Environment.CreateCoreWebView2ControllerOptions](corewebview2environment.md#createcorewebview2controlleroptions).

## Summary

Members|Description
--|--
[AllowHostInputProcessing](#allowhostinputprocessing) | Allows user input messages to pass through the browser window to be received by an app process window.
[DefaultBackgroundColor](#defaultbackgroundcolor) | Gets or sets the WebView2 default background color early during initialization.
[IsInPrivateModeEnabled](#isinprivatemodeenabled) | Manage the controller's InPrivate mode.
[ProfileName](#profilename) | Manage the name of the controller's profile.
[ScriptLocale](#scriptlocale) | Manages the value of the controller's script locale.

## Properties

### AllowHostInputProcessing

>  bool AllowHostInputProcessing

Allows user input messages to pass through the browser window to be received by an app process window.
The property is to enable/disable input passing through the app before being delivered to the WebView2. Setting this property to `TRUE` allows default .NET event handling API of WebView2 control to work, such as [PreProcessMessage](/dotnet/api/system.windows.forms.control.preprocessmessage) and [ProcessCmdKey](/dotnet/api/system.windows.forms.control.processcmdkey). This property is only applicable to controllers created with `CoreWebView2Environment.CreateCoreWebView2ControllerAsync` and not composition controllers created with `CoreWebView2Environment.CreateCoreWebView2CompositionControllerAsync`. By default the value is `FALSE`.

### DefaultBackgroundColor

>  [Color](/uwp/api/Windows.UI.Color) DefaultBackgroundColor

Gets or sets the WebView2 default background color early during initialization.
This API allows users to initialize the `DefaultBackgroundColor` early, preventing a white flash that can occur while WebView2 is loading when the background color is set to something other than white. With early initialization, the color remains consistent from the start. After initialization, it will return the set value.
The `DefaultBackgroundColor` is the color that renders underneath all web content. This means WebView2 renders this color when there is no web content loaded. When no background color is defined in WebView2, it uses the `DefaultBackgroundColor` property to render the background.By default, this color is set to white. This API only supports opaque colors and full transparency. It will fail for colors with alpha values that don't equal 0 or 255. When WebView2 is set to be fully transparent, it does not render a background, allowing the content from windows behind it to be visible.

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
