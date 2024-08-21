---
description: Indicates the kind of browsing data to clear. Or operations can be applied to create a mask representing multiple CoreWebView2BrowsingDataKinds. The resulting mask may be passed to CoreWebView2Profile.ClearBrowsingDataAsync to clear the corresponding data.
title: CoreWebView2BrowsingDataKinds
ms.date: 08/26/2024
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2BrowsingDataKinds
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- Microsoft.Web.WebView2.Core.CoreWebView2BrowsingDataKinds
---

# CoreWebView2BrowsingDataKinds Enum

Indicates the kind of browsing data to clear. Or operations can be applied to create a mask representing multiple CoreWebView2BrowsingDataKinds. The resulting mask may be passed to [CoreWebView2Profile.ClearBrowsingDataAsync](corewebview2profile.md#clearbrowsingdataasync) to clear the corresponding data.

| Name |  Value | Description |
|--|--|--|
|`FileSystems` | 0x1  |  Specifies file systems data.|
|`IndexedDb` | 0x2  |  Specifies data stored by the IndexedDB DOM feature.|
|`LocalStorage` | 0x4  |  Specifies data stored by the localStorage DOM API.|
|`WebSql` | 0x8  |  Specifies data stored by the Web SQL database DOM API.|
|`CacheStorage` | 0x10  |  Specifies data stored by the CacheStorage DOM API.|
|`AllDomStorage` | 0x20  |  Specifies DOM storage data, now and future. This browsing data kind is inclusive of CoreWebView2BrowsingDataKinds.FileSystems, CoreWebView2BrowsingDataKinds.IndexedDb, CoreWebView2BrowsingDataKinds.WebSql, CoreWebView2BrowsingDataKinds.ServiceWorkers, CoreWebView2BrowsingDataKinds.CacheStorage, and some other data kinds not listed yet to keep consistent with [DOM-accessible storage](https://www.w3.org/TR/clear-site-data/#storage).|
|`Cookies` | 0x40  |  Specifies HTTP cookies data.|
|`AllSite` | 0x80  |  Specifies all site data, now and future. This browsing data kind is inclusive of CoreWebView2BrowsingDataKinds.AllDomStorage and CoreWebView2BrowsingDataKinds.Cookies. New site data types may be added to this data kind in the future.|
|`DiskCache` | 0x100  |  Specifies disk cache.|
|`DownloadHistory` | 0x200  |  Specifies download history data.|
|`GeneralAutofill` | 0x400  |  Specifies general autofill form data. This excludes password information and includes information like: names, street and email addresses, phone numbers, and arbitrary input. This also includes payment data.|
|`PasswordAutosave` | 0x800  |  Specifies password autosave data.|
|`BrowsingHistory` | 0x1000  |  Specifies browsing history data.|
|`Settings` | 0x2000  |  Specifies settings data.|
|`AllProfile` | 0x4000  |  Specifies profile data that should be wiped to make it look like a new profile. This does not delete account-scoped data like passwords but will remove access to account-scoped data by signing the user out. Specifies all profile data, now and future. New profile data types may be added to this data kind in the future. This browsing data kind is inclusive of CoreWebView2BrowsingDataKinds.AllSite, CoreWebView2BrowsingDataKinds.DiskCache, CoreWebView2BrowsingDataKinds.DownloadHistory, CoreWebView2BrowsingDataKinds.GeneralAutofill, CoreWebView2BrowsingDataKinds.PasswordAutosave, CoreWebView2BrowsingDataKinds.BrowsingHistory, CoreWebView2BrowsingDataKinds.Settings.|
|`ServiceWorkers` | 0x8000  |  Specifies service workers registered for an origin, and clear will result in termination and deregistration of them.|


## Referenced by

- [CoreWebView2Profile](corewebview2profile.md)
