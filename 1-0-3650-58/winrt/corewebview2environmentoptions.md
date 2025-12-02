---
description: Options used to create WebView2 Environment.
title: CoreWebView2EnvironmentOptions
ms.date: 12/02/2025
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2EnvironmentOptions
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2EnvironmentOptions
- CoreWebView2EnvironmentOptions.AdditionalBrowserArguments
- CoreWebView2EnvironmentOptions.AllowSingleSignOnUsingOSPrimaryAccount
- CoreWebView2EnvironmentOptions.AreBrowserExtensionsEnabled
- CoreWebView2EnvironmentOptions.ChannelSearchKind
- CoreWebView2EnvironmentOptions.CustomSchemeRegistrations
- CoreWebView2EnvironmentOptions.EnableTrackingPrevention
- CoreWebView2EnvironmentOptions.ExclusiveUserDataFolderAccess
- CoreWebView2EnvironmentOptions.IsCustomCrashReportingEnabled
- CoreWebView2EnvironmentOptions.Language
- CoreWebView2EnvironmentOptions.ReleaseChannels
- CoreWebView2EnvironmentOptions.ScrollBarStyle
- CoreWebView2EnvironmentOptions.TargetCompatibleBrowserVersion
---

# CoreWebView2EnvironmentOptions Class



Options used to create WebView2 Environment.
Default values will use your defaulted Edge WebView2 Runtime binaries and user data folder.

## Summary

Members|Description
--|--
[AdditionalBrowserArguments](#additionalbrowserarguments) | Gets or sets the additional browser arguments to change the behavior of the WebView.
[AllowSingleSignOnUsingOSPrimaryAccount](#allowsinglesignonusingosprimaryaccount) | Determines whether to enable single sign on with Azure Active Directory (AAD) resources inside WebView using the logged in Windows account and single sign on (SSO) with web sites using Microsoft account associated with the login in Windows account.
[AreBrowserExtensionsEnabled](#arebrowserextensionsenabled) | Enable/disable browser extensions.
[ChannelSearchKind](#channelsearchkind) | Set `ChannelSearchKind` to `CoreWebView2ChannelSearchKind.LeastStable` so that the WebView2 loader searches for binaries from least to most stable: Canary -> Dev -> Beta -> WebView2 Runtime.
[CustomSchemeRegistrations](#customschemeregistrations) | A list of custom scheme registrations to be applied to the [CoreWebView2Environment](corewebview2environment.md).
[EnableTrackingPrevention](#enabletrackingprevention) | The EnableTrackingPrevention property is used to enable/disable tracking prevention feature in WebView2. This property enable/disable tracking prevention for all the WebView2's created in the same environment. By default this feature is enabled to block potentially harmful trackers and trackers from sites that aren't visited before and set to [CoreWebView2TrackingPreventionLevel](corewebview2trackingpreventionlevel.md).Balanced or whatever value was last changed/persisted on the profile.
[ExclusiveUserDataFolderAccess](#exclusiveuserdatafolderaccess) | Determines whether other processes can create [CoreWebView2Controller](corewebview2controller.md) from [CoreWebView2Environment](corewebview2environment.md) created with the same user data folder and therefore sharing the same WebView browser process instance.
[IsCustomCrashReportingEnabled](#iscustomcrashreportingenabled) | When `IsCustomCrashReportingEnabled` is set to `true`, Windows won't send crash data to Microsoft endpoint.
[Language](#language) | Gets or sets the default display language for WebView.
[ReleaseChannels](#releasechannels) | Sets the `ReleaseChannels`, which is a mask of one or more `CoreWebView2ReleaseChannels` indicating which channels environment creation should search for.
[ScrollBarStyle](#scrollbarstyle) | Set ScrollBar style to be used.
[TargetCompatibleBrowserVersion](#targetcompatiblebrowserversion) | Gets or sets the version of the WebView2 Runtime binaries required to be compatible with your app.

## Properties

### AdditionalBrowserArguments

>  string AdditionalBrowserArguments

Gets or sets the additional browser arguments to change the behavior of the WebView.
The arguments are passed to the browser process as part of the command. For more information about using command-line switches with Chromium browser processes, navigate to [Run Chromium with Flags](https://aka.ms/RunChromiumWithFlags). The value appended to a switch is appended to the browser process, for example, in `--edge-webview-switches=xxx` the value is `xxx`. If you specify a switch that is important to WebView functionality, it is ignored, for example, `--user-data-dir`. Specific features are disabled internally and blocked from being enabled. If a switch is specified multiple times, only the last instance is used.

A merge of the different values of the same switch is not attempted, except for disabled and enabled features. The features specified by `--enable-features` and `--disable-features` will be merged with simple logic:

- The features are the union of the specified features and built-in features. If a feature is disabled, it is removed from the enabled features list.
If you specify command-line switches and sets this property, the `--edge-webview-switches` value takes precedence and is processed last. If a switch fails to parse, the switch is ignored. The default state for the operation is to run the browser process with no extra flags.
Please note that calling this API twice will replace the previous value rather than appending to it. If there are multiple switches, there should be a space in between them. The one exception is if multiple features are being enabled/disabled for a single switch, in which case the features should be comma-separated. Ex. "--disable-features=feature1,feature2 --some-other-switch --do-something"

### AllowSingleSignOnUsingOSPrimaryAccount

>  bool AllowSingleSignOnUsingOSPrimaryAccount

Determines whether to enable single sign on with Azure Active Directory (AAD) resources inside WebView using the logged in Windows account and single sign on (SSO) with web sites using Microsoft account associated with the login in Windows account.
The default value is `false`. Universal Windows Platform apps must also declare `enterpriseCloudSSO` [restricted capability](/windows/uwp/packaging/app-capability-declarations#restricted-capabilities) for the single sign on (SSO) to work.

### AreBrowserExtensionsEnabled

>  bool AreBrowserExtensionsEnabled

Enable/disable browser extensions.
When `AreBrowserExtensionsEnabled` is set to `true`, new extensions can be added to user profile and used. `AreBrowserExtensionsEnabled` is default to be `false`, in this case, new extensions can't be installed, and already installed extension won't be available to use in user profile. If connecting to an already running environment with a different value for `AreBrowserExtensionsEnabled` property, it will fail with `HRESULT_FROM_WIN32(ERROR_INVALID_STATE)`. See [CoreWebView2BrowserExtension](corewebview2browserextension.md) for Extensions API details.

### ChannelSearchKind

>  [CoreWebView2ChannelSearchKind](corewebview2channelsearchkind.md) ChannelSearchKind

Set `ChannelSearchKind` to `CoreWebView2ChannelSearchKind.LeastStable` so that the WebView2 loader searches for binaries from least to most stable: Canary -> Dev -> Beta -> WebView2 Runtime.
The `ChannelSearchKind` property is `CoreWebView2ChannelSearchKind.MostStable` by default and environment creation searches for a release channel on the machine from most to least stable using the first channel found. The default search order is: WebView2 Release -> Beta -> Dev -> Canary. Set `ChannelSearchKind` to `CoreWebView2ChannelSearchKind.LeastStable` to reverse the search order so that environment creation searches for a channel from least to most stable. If a `ReleaseChannels` has been provided, environment creation will only search for channels in the set. See [CoreWebView2ReleaseChannels](corewebview2releasechannels.md) for more details on channels. This property can be overridden by the corresponding registry key `ChannelSearchKind` or the environment variable `WEBVIEW2_CHANNEL_SEARCH_KIND`. Set the value to `1` to reverse the search order. See [CoreWebView2Environment.CreateAsync](corewebview2environment.md#createasync) for more details on overrides.

### CustomSchemeRegistrations

>  [`IVector`](/uwp/api/Windows.Foundation.Collections.IVector-1)&lt;[CoreWebView2CustomSchemeRegistration](corewebview2customschemeregistration.md)&gt; CustomSchemeRegistrations

A list of custom scheme registrations to be applied to the [CoreWebView2Environment](corewebview2environment.md).

### EnableTrackingPrevention

>  bool EnableTrackingPrevention

The EnableTrackingPrevention property is used to enable/disable tracking prevention feature in WebView2. This property enable/disable tracking prevention for all the WebView2's created in the same environment. By default this feature is enabled to block potentially harmful trackers and trackers from sites that aren't visited before and set to [CoreWebView2TrackingPreventionLevel](corewebview2trackingpreventionlevel.md).Balanced or whatever value was last changed/persisted on the profile.
You can set this property to false to disable the tracking prevention feature if the app only renders content in the WebView2 that is known to be safe. Disabling this feature when creating environment also improves runtime performance by skipping related code.

You shouldn't disable this property if WebView2 is being used as a "full browser" with arbitrary navigation and should protect end user privacy.

There is [CoreWebView2Profile.PreferredTrackingPreventionLevel](corewebview2profile.md#preferredtrackingpreventionlevel) property to control levels of tracking prevention of the WebView2's associated with a same profile. However, you can also disable tracking prevention later using [CoreWebView2Profile.PreferredTrackingPreventionLevel](corewebview2profile.md#preferredtrackingpreventionlevel) property and [CoreWebView2TrackingPreventionLevel](corewebview2trackingpreventionlevel.md).None value but that doesn't improves runtime performance.

See [CoreWebView2Profile.PreferredTrackingPreventionLevel](corewebview2profile.md#preferredtrackingpreventionlevel) for more details.

Tracking prevention protects users from online tracking by restricting the ability of trackers to access browser-based storage as well as the network. See [Tracking prevention](/microsoft-edge/web-platform/tracking-prevention).

### ExclusiveUserDataFolderAccess

>  bool ExclusiveUserDataFolderAccess

Determines whether other processes can create [CoreWebView2Controller](corewebview2controller.md) from [CoreWebView2Environment](corewebview2environment.md) created with the same user data folder and therefore sharing the same WebView browser process instance.
The default value is `false`.

### IsCustomCrashReportingEnabled

>  bool IsCustomCrashReportingEnabled

When `IsCustomCrashReportingEnabled` is set to `true`, Windows won't send crash data to Microsoft endpoint.
The default value is `false`. In this case, WebView will respect OS consent.

### Language

>  string Language

Gets or sets the default display language for WebView.
It applies to browser UIs such as context menu and dialogs. It also applies to the `accept-languages` HTTP header that WebView sends to websites. The intended locale value is in the format of BCP 47 Language Tags. More information can be found from [IETF BCP47](https://www.ietf.org/rfc/bcp/bcp47.html).

### ReleaseChannels

>  [CoreWebView2ReleaseChannels](corewebview2releasechannels.md) ReleaseChannels

Sets the `ReleaseChannels`, which is a mask of one or more `CoreWebView2ReleaseChannels` indicating which channels environment creation should search for.
OR operation(s) can be applied to multiple `CoreWebView2ReleaseChannels` to create a mask. The default value is a mask of all the channels. By default, environment creation searches for channels from most to least stable, using the first channel found on the device. When `ReleaseChannels` is provided, environment creation will only search for the channels specified in the set. Set `ChannelSearchKind` to `CoreWebView2ChannelSearchKind.LeastStable` to reverse the search order so that environment creation searches for the least stable build first. See [CoreWebView2ReleaseChannels](corewebview2releasechannels.md) for descriptions of each channel. Environment creation fails if it is unable to find any channel from the `ReleaseChannels` installed on the device. Use <see cref="CoreWebView2Environment.GetAvailableBrowserVersionString(string, CoreWebView2EnvironmentOptions)"/> to verify which channel is used. If both a `BrowserExecutableFolder` and `ReleaseChannels` are provided, the `BrowserExecutableFolder` takes precedence. The `ReleaseChannels` can be overridden by the corresponding registry override `ReleaseChannels` or the environment variable `WEBVIEW2_RELEASE_CHANNELS`. Set the value to a comma-separated string of integers, which map to the following release channel values: Stable (0), Beta (1), Dev (2), and Canary (3). For example, the values "0,2" and "2,0" indicate that environment creation should only search for Dev channel and the WebView2 Runtime, using the order indicated by [CoreWebView2EnvironmentOptions.ChannelSearchKind](corewebview2environmentoptions.md#channelsearchkind). Environment creation attempts to interpret each integer and treats any invalid entry as Stable channel.

|   ReleaseChannels   |   Channel Search Kind: Most Stable (default)   |   Channel Search Kind: Least Stable   |
| --- | --- | --- |
|CoreWebView2ReleaseChannels.Beta \| CoreWebView2ReleaseChannels.Stable| WebView2 Runtime -> Beta | Beta -> WebView2 Runtime|
|CoreWebView2ReleaseChannels.Canary \| CoreWebView2ReleaseChannels.Dev \| CoreWebView2ReleaseChannels.Beta \| CoreWebView2ReleaseChannels.Stable | WebView2 Runtime -> Beta -> Dev -> Canary | Canary -> Dev -> Beta -> WebView2 Runtime |
|CoreWebView2ReleaseChannels.Canary| Canary | Canary |
|CoreWebView2ReleaseChannels.Beta \| CoreWebView2ReleaseChannels.Canary \| CoreWebView2ReleaseChannels.Stable | WebView2 Runtime -> Beta -> Canary | Canary -> Beta -> WebView2 Runtime |

### ScrollBarStyle

>  [CoreWebView2ScrollbarStyle](corewebview2scrollbarstyle.md) ScrollBarStyle

Set ScrollBar style to be used.
The default is `CoreWebView2ScrollbarStyle.Default` which specifies the default browser ScrollBar style. CSS styles that modify the ScrollBar applied on top of native ScrollBar styling that is selected with `CoreWebView2ScrollbarStyle`.

### TargetCompatibleBrowserVersion

>  string TargetCompatibleBrowserVersion

Gets or sets the version of the WebView2 Runtime binaries required to be compatible with your app.
This defaults to the WebView2 Runtime version that corresponds with the version of the SDK the app is using. The format of this value is the same as the format of the [CoreWebView2Environment.BrowserVersionString](corewebview2environment.md#browserversionstring) property and other BrowserVersion values. Only the version part of the BrowserVersion value is respected. The channel suffix, if it exists, is ignored. The version of the WebView2 Runtime binaries actually used may be different from the specified TargetCompatibleBrowserVersion. The binaries are only guaranteed to be compatible. Verify the actual version on the [CoreWebView2Environment.BrowserVersionString](corewebview2environment.md#browserversionstring) property.


## Constructors
### CoreWebView2EnvironmentOptions

>  CoreWebView2EnvironmentOptions()







## Referenced by

- [CoreWebView2Environment](corewebview2environment.md)
