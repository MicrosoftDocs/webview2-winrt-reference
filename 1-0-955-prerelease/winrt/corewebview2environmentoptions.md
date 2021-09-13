---
description: Options used to create WebView2 Environment.
title: CoreWebView2EnvironmentOptions
ms.date: 08/16/2021
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2EnvironmentOptions
---

# CoreWebView2EnvironmentOptions Class



Options used to create WebView2 Environment.
Default values will use your defaulted Edge WebView2 Runtime binaries and user data folder.

## Summary

Members|Description
--|--
[AdditionalBrowserArguments](#additionalbrowserarguments) | Gets or sets the additional browser arguments to change the behavior of the WebView.
[AllowSingleSignOnUsingOSPrimaryAccount](#allowsinglesignonusingosprimaryaccount) | Determines whether to enable single sign on with Azure Active Directory (AAD) resources inside WebView using the logged in Windows account and single sign on (SSO) with web sites using Microsoft account associated with the login in Windows account.
[Language](#language) | Gets or sets the default display language for WebView.
[TargetCompatibleBrowserVersion](#targetcompatiblebrowserversion) | Gets or sets the version of the WebView2 Runtime binaries required to be compatible with the your app.

## Properties

### AdditionalBrowserArguments

>  string AdditionalBrowserArguments

Gets or sets the additional browser arguments to change the behavior of the WebView.

The arguments are passed to the browser process as part of the command. For more information about using command-line switches with Chromium browser processes, navigate to [Run Chromium with Flags](https://aka.ms/RunChromiumWithFlags). The value appended to a switch is appended to the browser process, for example, in `--edge-webview-switches=xxx` the value is `xxx`. If you specify a switch that is important to WebView functionality, it is ignore, for example, `--user-data-dir`. Specific features are disabled internally and blocked from being enabled. If a switch is specified multiple times, only the last instance is used.

A merge of the different values of the same switch is not attempted, except for disabled and enabled features. The features specified by `--enable-features` and `--disable-features` will be merged with simple logic:

- The features are the union of the specified features and built-in features. If a feature is disabled, it is removed from the enabled features list.

If you specify command-line switches and sets this property, the `--edge-webview-switches` value takes precedence and is processed last. If a switch fails to parse, the switch is ignored. The default state for the operation is to run the browser process with no extra flags.


### AllowSingleSignOnUsingOSPrimaryAccount

>  bool AllowSingleSignOnUsingOSPrimaryAccount

Determines whether to enable single sign on with Azure Active Directory (AAD) resources inside WebView using the logged in Windows account and single sign on (SSO) with web sites using Microsoft account associated with the login in Windows account.

The default value is `false`. Universal Windows Platform apps must also declare `enterpriseCloudSSO` [restricted capability](/windows/uwp/packaging/app-capability-declarations#restricted-capabilities) for the single sign on (SSO) to work.

### Language

>  string Language

Gets or sets the default display language for WebView.

It applies to browser UIs such as context menu and dialogs. It also applies to the `accept-languages` HTTP header that WebView sends to websites. It is in the format of `language[-country]` where `language` is the 2-letter code from [ISO 639](https://www.iso.org/iso-639-language-codes.html) and `country` is the 2-letter code from [ISO 3166](https://www.iso.org/standard/72482.html).

### TargetCompatibleBrowserVersion

>  string TargetCompatibleBrowserVersion

Gets or sets the version of the WebView2 Runtime binaries required to be compatible with the your app.

This defaults to the WebView2 Runtime version that corresponds with the version of the SDK the app is using. The format of this value is the same as the format of the [CoreWebView2Environment.BrowserVersionString](corewebview2environment.md#browserversionstring) property and other BrowserVersion values. Only the version part of the BrowserVersion value is respected. The channel suffix, if it exists, is ignored. The version of the WebView2 Runtime binaries actually used may be different from the specified TargetCompatibleBrowserVersion. They binaries are only guaranteed to be compatible. Verify the actual version on the [CoreWebView2Environment.BrowserVersionString](corewebview2environment.md#browserversionstring) property.


## Constructors
### CoreWebView2EnvironmentOptions

>  CoreWebView2EnvironmentOptions()







## Referenced by

- [CoreWebView2Environment](corewebview2environment.md)
