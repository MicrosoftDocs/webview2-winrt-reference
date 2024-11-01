---
title: CoreWebView2Profile
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/01/2024
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2Profile
---

# runtimeClass CoreWebView2Profile



## Summary

Members|Description
--|--
[CookieManager](#cookiemanager) | 
[DefaultDownloadFolderPath](#defaultdownloadfolderpath) | 
[IsGeneralAutofillEnabled](#isgeneralautofillenabled) | 
[IsInPrivateModeEnabled](#isinprivatemodeenabled) | 
[IsPasswordAutosaveEnabled](#ispasswordautosaveenabled) | 
[PreferredColorScheme](#preferredcolorscheme) | 
[PreferredTrackingPreventionLevel](#preferredtrackingpreventionlevel) | 
[ProfileName](#profilename) | 
[ProfilePath](#profilepath) | 
[AddBrowserExtensionAsync](#addbrowserextensionasync) | 
[ClearBrowsingDataAsync](#clearbrowsingdataasync) | 
[ClearBrowsingDataAsync](#clearbrowsingdataasync) | 
[ClearBrowsingDataAsync](#clearbrowsingdataasync) | 
[ClearCustomDataPartitionAsync](#clearcustomdatapartitionasync) | 
[Delete](#delete) | 
[GetBrowserExtensionsAsync](#getbrowserextensionsasync) | 
[GetNonDefaultPermissionSettingsAsync](#getnondefaultpermissionsettingsasync) | 
[SetPermissionStateAsync](#setpermissionstateasync) | 
[Deleted](#deleted) | 

## Properties

### CookieManager

> readonly  [CoreWebView2CookieManager](corewebview2cookiemanager.md) CookieManager

### DefaultDownloadFolderPath

>  string DefaultDownloadFolderPath

### IsGeneralAutofillEnabled

>  bool IsGeneralAutofillEnabled

### IsInPrivateModeEnabled

> readonly  bool IsInPrivateModeEnabled

### IsPasswordAutosaveEnabled

>  bool IsPasswordAutosaveEnabled

### PreferredColorScheme

>  [CoreWebView2PreferredColorScheme](corewebview2preferredcolorscheme.md) PreferredColorScheme

### PreferredTrackingPreventionLevel

>  [CoreWebView2TrackingPreventionLevel](corewebview2trackingpreventionlevel.md) PreferredTrackingPreventionLevel

### ProfileName

> readonly  string ProfileName

### ProfilePath

> readonly  string ProfilePath



## Methods

### AddBrowserExtensionAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;[CoreWebView2BrowserExtension](corewebview2browserextension.md)&gt; AddBrowserExtensionAsync(string operation)



### ClearBrowsingDataAsync

> [IAsyncAction](/uwp/api/Windows.Foundation.IAsyncAction) ClearBrowsingDataAsync([CoreWebView2BrowsingDataKinds](corewebview2browsingdatakinds.md) operation, [DateTime](/uwp/api/Windows.Foundation.DateTime) dataKinds, [DateTime](/uwp/api/Windows.Foundation.DateTime) startTime)



### ClearBrowsingDataAsync

> [IAsyncAction](/uwp/api/Windows.Foundation.IAsyncAction) ClearBrowsingDataAsync()



### ClearBrowsingDataAsync

> [IAsyncAction](/uwp/api/Windows.Foundation.IAsyncAction) ClearBrowsingDataAsync([CoreWebView2BrowsingDataKinds](corewebview2browsingdatakinds.md) operation)



### ClearCustomDataPartitionAsync

> [IAsyncAction](/uwp/api/Windows.Foundation.IAsyncAction) ClearCustomDataPartitionAsync(string operation)



### Delete

> void Delete()



### GetBrowserExtensionsAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;[`IVectorView`](/uwp/api/Windows.Foundation.Collections.IVectorView-1)&lt;[CoreWebView2BrowserExtension](corewebview2browserextension.md)&gt;&gt; GetBrowserExtensionsAsync()



### GetNonDefaultPermissionSettingsAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;[`IVectorView`](/uwp/api/Windows.Foundation.Collections.IVectorView-1)&lt;[CoreWebView2PermissionSetting](corewebview2permissionsetting.md)&gt;&gt; GetNonDefaultPermissionSettingsAsync()



### SetPermissionStateAsync

> [IAsyncAction](/uwp/api/Windows.Foundation.IAsyncAction) SetPermissionStateAsync([CoreWebView2PermissionKind](corewebview2permissionkind.md) operation, string PermissionKind, [CoreWebView2PermissionState](corewebview2permissionstate.md) origin)




## Events

### Deleted

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2Profile](corewebview2profile.md), Object&gt;



## Referenced by

- [CoreWebView2](corewebview2.md)
