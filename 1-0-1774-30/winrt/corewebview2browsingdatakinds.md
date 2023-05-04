---
title: CoreWebView2BrowsingDataKinds
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2023
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2BrowsingDataKinds
---

# enum CoreWebView2BrowsingDataKinds

Indicates the kind of browsing data to clear. Or operations can be applied to create a mask representing multiple CoreWebView2BrowsingDataKinds. The resulting mask may be passed to [CoreWebView2Profile.ClearBrowsingDataAsync](corewebview2profile.md#clearbrowsingdataasync) to clear the corresponding data.

| Name |  Value | Description |
|--|--|--|
|`FileSystems` | 0x1  |  Specifies file systems data.|
|`IndexedDb` | 0x2  |  Specifies data stored by the IndexedDB DOM feature.|
|`LocalStorage` | 0x4  |  Specifies data stored by the localStorage DOM API.|
|`WebSql` | 0x8  |  Specifies data stored by the Web SQL database DOM API.|
|`CacheStorage` | 0x10  |  Specifies data stored by the CacheStorage DOM API.|
|`AllDomStorage` | 0x20  |  Specifies DOM storage data, now and future. This browsing data kind is inclusive of CoreWebView2BrowsingDataKinds.FileSystems, CoreWebView2BrowsingDataKinds.IndexedDb, CoreWebView2BrowsingDataKinds.WebSql, CoreWebView2BrowsingDataKinds.CacheStorage. New DOM storage data types may be added to this data kind in the future.|
|`Cookies` | 0x40  |  Specifies HTTP cookies data.|
|`AllSite` | 0x80  |  Specifies all site data, now and future. This browsing data kind is inclusive of CoreWebView2BrowsingDataKinds.AllDomStorage and CoreWebView2BrowsingDataKinds.Cookies. New site data types may be added to this data kind in the future.|
|`DiskCache` | 0x100  |  Specifies disk cache.|
|`DownloadHistory` | 0x200  |  Specifies download history data.|
|`GeneralAutofill` | 0x400  |  Specifies general autofill form data. This excludes password information and includes information like: names, street and email addresses, phone numbers, and arbitrary input. This also includes payment data.|
|`PasswordAutosave` | 0x800  |  Specifies password autosave data.|
|`BrowsingHistory` | 0x1000  |  Specifies browsing history data.|
|`Settings` | 0x2000  |  Specifies settings data.|
|`AllProfile` | 0x4000  |  Specifies profile data that should be wiped to make it look like a new profile. This does not delete account-scoped data like passwords but will remove access to account-scoped data by signing the user out. Specifies all profile data, now and future. New profile data types may be added to this data kind in the future. This browsing data kind is inclusive of [CoreWebView2BrowsingDataKinds](corewebview2browsingdatakinds.md).AllSite, [CoreWebView2BrowsingDataKinds](corewebview2browsingdatakinds.md).DiskCache, [CoreWebView2BrowsingDataKinds](corewebview2browsingdatakinds.md).DownloadHistory, [CoreWebView2BrowsingDataKinds](corewebview2browsingdatakinds.md).GeneralAutofill, [CoreWebView2BrowsingDataKinds](corewebview2browsingdatakinds.md).PasswordAutosave, [CoreWebView2BrowsingDataKinds](corewebview2browsingdatakinds.md).BrowsingHistory, [CoreWebView2BrowsingDataKinds](corewebview2browsingdatakinds.md).Settings.|


## Referenced by

- [CoreWebView2Profile](corewebview2profile.md)
