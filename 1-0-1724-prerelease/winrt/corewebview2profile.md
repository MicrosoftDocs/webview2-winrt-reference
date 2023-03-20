---
description: Multiple profiles can be created under a single user data directory but with separated cookies, user preference settings, and various data storage etc.. If the CoreWebView2 was created with a CoreWebView2ControllerOptions, the CoreWebView2Profile will match those specified options. Otherwise if this CoreWebView2 was created without a CoreWebView2ControllerOptions, then this will be the default CoreWebView2Profile for the corresponding CoreWebView2Environment.
title: CoreWebView2Profile
ms.date: 03/13/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2Profile
---

# CoreWebView2Profile Class



Multiple profiles can be created under a single user data directory but with separated cookies, user preference settings, and various data storage etc.. If the CoreWebView2 was created with a [CoreWebView2ControllerOptions](corewebview2controlleroptions.md), the CoreWebView2Profile will match those specified options. Otherwise if this CoreWebView2 was created without a [CoreWebView2ControllerOptions](corewebview2controlleroptions.md), then this will be the default CoreWebView2Profile for the corresponding CoreWebView2Environment.

## Summary

Members|Description
--|--
[CookieManager](#cookiemanager) | Get the [CoreWebView2CookieManager](corewebview2cookiemanager.md) which Creates, adds or updates, gets, or or view the cookies for the current profile.
[DefaultDownloadFolderPath](#defaultdownloadfolderpath) | The default download folder path.
[IsInPrivateModeEnabled](#isinprivatemodeenabled) | InPrivate mode is enabled or not.
[PreferredColorScheme](#preferredcolorscheme) | The PreferredColorScheme property sets the overall color scheme of the WebView2s associated with this profile.
[PreferredTrackingPreventionLevel](#preferredtrackingpreventionlevel) | The `PreferredTrackingPreventionLevel` property allows you to control levels of tracking prevention for WebView2 which are associated with a profile. This level would apply to the context of the profile. That is, all WebView2s sharing the same profile will be affected and also the value is persisted in the user data folder.
[ProfileName](#profilename) | The name of the profile.
[ProfilePath](#profilepath) | Full path of the profile directory.
[ClearBrowsingDataAsync](#clearbrowsingdataasync) | Clears browsing data for dataKinds between startTime and endTime.
[ClearBrowsingDataAsync](#clearbrowsingdataasync) | Clears all browsing data associated with the profile this method is called on regardless of timestamp.
[ClearBrowsingDataAsync](#clearbrowsingdataasync) | Clear the browsing data of the associated profile.
[ClearCustomDataPartitionAsync](#clearcustomdatapartitionasync) | Clears all DOM storage and cookies in the specified custom data partition.
[Delete](#delete) | Delete this profile.
[GetNonDefaultPermissionSettingsAsync](#getnondefaultpermissionsettingsasync) | Gets a list of nondefault permission settings.
[SetPermissionStateAsync](#setpermissionstateasync) | Sets permission state for the given permission kind and origin asynchronously.
[Deleted](#deleted) | Raised when profile is marked for deletion.

## Properties

### CookieManager

> readonly  [CoreWebView2CookieManager](corewebview2cookiemanager.md) CookieManager

Get the [CoreWebView2CookieManager](corewebview2cookiemanager.md) which Creates, adds or updates, gets, or or view the cookies for the current profile.
All CoreWebView2s associated with this profile share the same cookie values. Changes to cookies in this cookie manager apply to all CoreWebView2s associated with this profile.

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

### PreferredTrackingPreventionLevel

>  [CoreWebView2TrackingPreventionLevel](corewebview2trackingpreventionlevel.md) PreferredTrackingPreventionLevel

The `PreferredTrackingPreventionLevel` property allows you to control levels of tracking prevention for WebView2 which are associated with a profile. This level would apply to the context of the profile. That is, all WebView2s sharing the same profile will be affected and also the value is persisted in the user data folder.

See [CoreWebView2TrackingPreventionLevel](corewebview2trackingpreventionlevel.md) for descriptions of levels.
If tracking prevention feature is enabled when creating the WebView2 environment, you can also disable tracking prevention later using this property and [CoreWebView2TrackingPreventionLevel](corewebview2trackingpreventionlevel.md).None value but that doesn't improves runtime performance.

There is [CoreWebView2EnvironmentOptions.EnableTrackingPrevention](corewebview2environmentoptions.md#enabletrackingprevention) property to enable/disable tracking prevention feature for all the WebView2's created in the same environment. If enabled, PreferredTrackingPreventionLevel is set to [CoreWebView2TrackingPreventionLevel](corewebview2trackingpreventionlevel.md).Balanced by default for all the WebView2's and profiles created in the same environment or is set to the level whatever value was last changed/persisted to the profile. If disabled PreferredTrackingPreventionLevel is not respected by WebView2. If PreferredTrackingPreventionLevel is set when the feature is disabled, the property value get changed and persisted but it will takes effect only if [CoreWebView2EnvironmentOptions.EnableTrackingPrevention](corewebview2environmentoptions.md#enabletrackingprevention) is true.

See [CoreWebView2EnvironmentOptions.EnableTrackingPrevention](corewebview2environmentoptions.md#enabletrackingprevention) for more details.

### ProfileName

> readonly  string ProfileName

The name of the profile.

### ProfilePath

> readonly  string ProfilePath

Full path of the profile directory.



## Methods

### ClearBrowsingDataAsync

> [IAsyncAction](/uwp/api/Windows.Foundation.IAsyncAction) ClearBrowsingDataAsync([CoreWebView2BrowsingDataKinds](corewebview2browsingdatakinds.md) dataKinds, [DateTime](/uwp/api/Windows.Foundation.DateTime) startTime, [DateTime](/uwp/api/Windows.Foundation.DateTime) endTime)

Clears browsing data for dataKinds between startTime and endTime.



### ClearBrowsingDataAsync

> [IAsyncAction](/uwp/api/Windows.Foundation.IAsyncAction) ClearBrowsingDataAsync()

Clears all browsing data associated with the profile this method is called on regardless of timestamp.



### ClearBrowsingDataAsync

> [IAsyncAction](/uwp/api/Windows.Foundation.IAsyncAction) ClearBrowsingDataAsync([CoreWebView2BrowsingDataKinds](corewebview2browsingdatakinds.md) dataKinds)

Clear the browsing data of the associated profile.
Clears browsing data on the profile the method is called on. Additional optional parameters include the start time and end time to clear the browsing data between as well as the data specific data kinds to clear on the profile. The method may be overloaded to take:

- No parameters - in which the entirety of the data on the profile will be cleared.
- The data kind(s) - in which the data kind(s) will be cleared for their entirety.
- The data kind(s), start time, and end time - in which the data kind(s) will be cleared between the start and end time. The start time will be offset by -1.0 and the end time will be offset by +1.0 to include the last fractional second on each respective end. The start time is inclusive in the time period while the end time is exclusive.

The exposed methods are as follows:
```
ClearBrowsingDataAsync(CoreWebView2BrowsingDataKinds dataKinds);
ClearBrowsingDataAsync(CoreWebView2BrowsingDataKinds dataKinds, DateTime startTime, DateTime endTime);
ClearBrowsingDataAsync();
```



### ClearCustomDataPartitionAsync

> [IAsyncAction](/uwp/api/Windows.Foundation.IAsyncAction) ClearCustomDataPartitionAsync(string CustomDataPartitionId)

Clears all DOM storage and cookies in the specified custom data partition.
Clears all DOM storage and cookies in the custom data partition identified by the `CustomDataPartitionId`.
If no partition is found for the specified `CustomDataPartitionId`, the API succeeds without doing anything.
As DOM storage and cookies in the custom data partition is also browsing data, they will also be cleared when [CoreWebView2Profile.ClearBrowsingDataAsync](corewebview2profile.md#clearbrowsingdataasync) is called and the clearing condition is met.
:::code language="csharp" source="../code/sample/SampleApps/WebView2WpfBrowser/MainWindow.xaml.cs" id="ClearCustomDataPartition":::



### Delete

> void Delete()

Delete this profile.
After the API is called, the profile will be marked for deletion. The local profile's directory will be deleted at browser process exit. If it fails to delete, because something else is holding the files open, WebView2 will try to delete the profile at all future browser process starts until successful. The corresponding CoreWebView2s will be closed and the CoreWebView2Profile.Deleted event will be raised. See `CoreWebView2Profile.Deleted` for more information. If you try to create a new profile with the same name as an existing profile that has been marked as deleted but hasn't yet been deleted, profile creation will fail with HRESULT_FROM_WIN32(ERROR_DELETE_PENDING).



### GetNonDefaultPermissionSettingsAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;[`IVectorView`](/uwp/api/Windows.Foundation.Collections.IVectorView-1)&lt;[CoreWebView2PermissionSetting](corewebview2permissionsetting.md)&gt;&gt; GetNonDefaultPermissionSettingsAsync()

Gets a list of nondefault permission settings.



### SetPermissionStateAsync

> [IAsyncAction](/uwp/api/Windows.Foundation.IAsyncAction) SetPermissionStateAsync([CoreWebView2PermissionKind](corewebview2permissionkind.md) PermissionKind, string origin, [CoreWebView2PermissionState](corewebview2permissionstate.md) State)

Sets permission state for the given permission kind and origin asynchronously.
The state change persists across sessions until it is changed by another call to `SetPermissionState`, or by setting the `State` property in `PermissionRequestedEventArgs`. Setting the state to [CoreWebView2PermissionState.Default](corewebview2permissionstate.md) will erase any state saved in the profile and restore the default behavior. The origin should have a valid scheme and host (e.g. "https://www.example.com"), otherwise the method fails. Additional URI parts like path and fragment are ignored. For example, "https://wwww.example.com/app1/index.html/" is treated the same as "https://wwww.example.com". See the [MDN origin definition](https://developer.mozilla.org/en-US/docs/Glossary/Origin) for more details.




## Events

### Deleted

Raised when profile is marked for deletion.
When this event is raised, the CoreWebView2Profile and its corresponding CoreWebView2s have been closed, and cannot be used anymore.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2Profile, Object&gt;



## Referenced by

- [CoreWebView2](corewebview2.md)
