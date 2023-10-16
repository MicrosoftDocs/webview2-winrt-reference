---
description: 
title: CoreWebView2Profile
ms.date: 10/16/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2Profile
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- Microsoft.Web.WebView2.Core.CoreWebView2Profile
- Microsoft.Web.WebView2.Core.CoreWebView2Profile.CookieManager
- Microsoft.Web.WebView2.Core.CoreWebView2Profile.DefaultDownloadFolderPath
- Microsoft.Web.WebView2.Core.CoreWebView2Profile.IsGeneralAutofillEnabled
- Microsoft.Web.WebView2.Core.CoreWebView2Profile.IsInPrivateModeEnabled
- Microsoft.Web.WebView2.Core.CoreWebView2Profile.IsPasswordAutosaveEnabled
- Microsoft.Web.WebView2.Core.CoreWebView2Profile.PreferredColorScheme
- Microsoft.Web.WebView2.Core.CoreWebView2Profile.PreferredTrackingPreventionLevel
- Microsoft.Web.WebView2.Core.CoreWebView2Profile.ProfileName
- Microsoft.Web.WebView2.Core.CoreWebView2Profile.ProfilePath
- Microsoft.Web.WebView2.Core.CoreWebView2Profile.ClearBrowsingDataAsync
- Microsoft.Web.WebView2.Core.CoreWebView2Profile.ClearBrowsingDataAsync
- Microsoft.Web.WebView2.Core.CoreWebView2Profile.ClearBrowsingDataAsync
- Microsoft.Web.WebView2.Core.CoreWebView2Profile.GetNonDefaultPermissionSettingsAsync
- Microsoft.Web.WebView2.Core.CoreWebView2Profile.SetPermissionStateAsync
- Microsoft.Web.WebView2.Core.CoreWebView2Profile.get_CookieManager
- Microsoft.Web.WebView2.Core.CoreWebView2Profile.get_DefaultDownloadFolderPath
- Microsoft.Web.WebView2.Core.CoreWebView2Profile.get_IsGeneralAutofillEnabled
- Microsoft.Web.WebView2.Core.CoreWebView2Profile.get_IsInPrivateModeEnabled
- Microsoft.Web.WebView2.Core.CoreWebView2Profile.get_IsPasswordAutosaveEnabled
- Microsoft.Web.WebView2.Core.CoreWebView2Profile.get_PreferredColorScheme
- Microsoft.Web.WebView2.Core.CoreWebView2Profile.get_PreferredTrackingPreventionLevel
- Microsoft.Web.WebView2.Core.CoreWebView2Profile.get_ProfileName
- Microsoft.Web.WebView2.Core.CoreWebView2Profile.get_ProfilePath
- Microsoft.Web.WebView2.Core.CoreWebView2Profile.put_DefaultDownloadFolderPath
- Microsoft.Web.WebView2.Core.CoreWebView2Profile.put_IsGeneralAutofillEnabled
- Microsoft.Web.WebView2.Core.CoreWebView2Profile.put_IsPasswordAutosaveEnabled
- Microsoft.Web.WebView2.Core.CoreWebView2Profile.put_PreferredColorScheme
- Microsoft.Web.WebView2.Core.CoreWebView2Profile.put_PreferredTrackingPreventionLevel
---

# CoreWebView2Profile Class



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
[ClearBrowsingDataAsync](#clearbrowsingdataasync) | 
[ClearBrowsingDataAsync](#clearbrowsingdataasync) | 
[ClearBrowsingDataAsync](#clearbrowsingdataasync) | 
[GetNonDefaultPermissionSettingsAsync](#getnondefaultpermissionsettingsasync) | 
[SetPermissionStateAsync](#setpermissionstateasync) | 

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

### ClearBrowsingDataAsync

> [IAsyncAction](/uwp/api/Windows.Foundation.IAsyncAction) ClearBrowsingDataAsync([CoreWebView2BrowsingDataKinds](corewebview2browsingdatakinds.md) dataKinds, [DateTime](/uwp/api/Windows.Foundation.DateTime) startTime, [DateTime](/uwp/api/Windows.Foundation.DateTime) endTime)



### ClearBrowsingDataAsync

> [IAsyncAction](/uwp/api/Windows.Foundation.IAsyncAction) ClearBrowsingDataAsync()



### ClearBrowsingDataAsync

> [IAsyncAction](/uwp/api/Windows.Foundation.IAsyncAction) ClearBrowsingDataAsync([CoreWebView2BrowsingDataKinds](corewebview2browsingdatakinds.md) dataKinds)



### GetNonDefaultPermissionSettingsAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;[`IVectorView`](/uwp/api/Windows.Foundation.Collections.IVectorView-1)&lt;[CoreWebView2PermissionSetting](corewebview2permissionsetting.md)&gt;&gt; GetNonDefaultPermissionSettingsAsync()



### SetPermissionStateAsync

> [IAsyncAction](/uwp/api/Windows.Foundation.IAsyncAction) SetPermissionStateAsync([CoreWebView2PermissionKind](corewebview2permissionkind.md) PermissionKind, string origin, [CoreWebView2PermissionState](corewebview2permissionstate.md) State)






## Referenced by

- [CoreWebView2](corewebview2.md)
