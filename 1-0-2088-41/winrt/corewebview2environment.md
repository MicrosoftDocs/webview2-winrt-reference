---
description: 
title: CoreWebView2Environment
ms.date: 10/16/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2Environment
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- Microsoft.Web.WebView2.Core.CoreWebView2Environment
- Microsoft.Web.WebView2.Core.CoreWebView2Environment.BrowserVersionString
- Microsoft.Web.WebView2.Core.CoreWebView2Environment.FailureReportFolderPath
- Microsoft.Web.WebView2.Core.CoreWebView2Environment.UserDataFolder
- Microsoft.Web.WebView2.Core.CoreWebView2Environment.CompareBrowserVersionString
- Microsoft.Web.WebView2.Core.CoreWebView2Environment.CreateAsync
- Microsoft.Web.WebView2.Core.CoreWebView2Environment.CreateContextMenuItem
- Microsoft.Web.WebView2.Core.CoreWebView2Environment.CreateCoreWebView2CompositionControllerAsync
- Microsoft.Web.WebView2.Core.CoreWebView2Environment.CreateCoreWebView2CompositionControllerAsync
- Microsoft.Web.WebView2.Core.CoreWebView2Environment.CreateCoreWebView2ControllerAsync
- Microsoft.Web.WebView2.Core.CoreWebView2Environment.CreateCoreWebView2ControllerAsync
- Microsoft.Web.WebView2.Core.CoreWebView2Environment.CreateCoreWebView2ControllerOptions
- Microsoft.Web.WebView2.Core.CoreWebView2Environment.CreateCoreWebView2PointerInfo
- Microsoft.Web.WebView2.Core.CoreWebView2Environment.CreatePrintSettings
- Microsoft.Web.WebView2.Core.CoreWebView2Environment.CreateSharedBuffer
- Microsoft.Web.WebView2.Core.CoreWebView2Environment.CreateWebResourceRequest
- Microsoft.Web.WebView2.Core.CoreWebView2Environment.CreateWebResourceResponse
- Microsoft.Web.WebView2.Core.CoreWebView2Environment.CreateWithOptionsAsync
- Microsoft.Web.WebView2.Core.CoreWebView2Environment.GetAvailableBrowserVersionString
- Microsoft.Web.WebView2.Core.CoreWebView2Environment.GetAvailableBrowserVersionString
- Microsoft.Web.WebView2.Core.CoreWebView2Environment.GetProcessInfos
- Microsoft.Web.WebView2.Core.CoreWebView2Environment.add_BrowserProcessExited
- Microsoft.Web.WebView2.Core.CoreWebView2Environment.add_NewBrowserVersionAvailable
- Microsoft.Web.WebView2.Core.CoreWebView2Environment.add_ProcessInfosChanged
- Microsoft.Web.WebView2.Core.CoreWebView2Environment.get_BrowserVersionString
- Microsoft.Web.WebView2.Core.CoreWebView2Environment.get_FailureReportFolderPath
- Microsoft.Web.WebView2.Core.CoreWebView2Environment.get_UserDataFolder
- Microsoft.Web.WebView2.Core.CoreWebView2Environment.remove_BrowserProcessExited
- Microsoft.Web.WebView2.Core.CoreWebView2Environment.remove_NewBrowserVersionAvailable
- Microsoft.Web.WebView2.Core.CoreWebView2Environment.remove_ProcessInfosChanged
- Microsoft.Web.WebView2.Core.CoreWebView2Environment.BrowserProcessExited
- Microsoft.Web.WebView2.Core.CoreWebView2Environment.NewBrowserVersionAvailable
- Microsoft.Web.WebView2.Core.CoreWebView2Environment.ProcessInfosChanged
---

# CoreWebView2Environment Class



## Summary

Members|Description
--|--
[BrowserVersionString](#browserversionstring) | 
[FailureReportFolderPath](#failurereportfolderpath) | 
[UserDataFolder](#userdatafolder) | 
[CompareBrowserVersionString](#comparebrowserversionstring) | 
[CreateAsync](#createasync) | 
[CreateContextMenuItem](#createcontextmenuitem) | 
[CreateCoreWebView2CompositionControllerAsync](#createcorewebview2compositioncontrollerasync) | 
[CreateCoreWebView2CompositionControllerAsync](#createcorewebview2compositioncontrollerasync) | 
[CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync) | 
[CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync) | 
[CreateCoreWebView2ControllerOptions](#createcorewebview2controlleroptions) | 
[CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo) | 
[CreatePrintSettings](#createprintsettings) | 
[CreateSharedBuffer](#createsharedbuffer) | 
[CreateWebResourceRequest](#createwebresourcerequest) | 
[CreateWebResourceResponse](#createwebresourceresponse) | 
[CreateWithOptionsAsync](#createwithoptionsasync) | 
[GetAvailableBrowserVersionString](#getavailablebrowserversionstring) | 
[GetAvailableBrowserVersionString](#getavailablebrowserversionstring) | 
[GetProcessInfos](#getprocessinfos) | 
[BrowserProcessExited](#browserprocessexited) | 
[NewBrowserVersionAvailable](#newbrowserversionavailable) | 
[ProcessInfosChanged](#processinfoschanged) | 

## Properties

### BrowserVersionString

> readonly  string BrowserVersionString

### FailureReportFolderPath

> readonly  string FailureReportFolderPath

### UserDataFolder

> readonly  string UserDataFolder



## Methods

### CompareBrowserVersionString

> static int CompareBrowserVersionString(string browserVersionString1, string browserVersionString2)



### CreateAsync

> static [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;CoreWebView2Environment&gt; CreateAsync()



### CreateContextMenuItem

> [CoreWebView2ContextMenuItem](corewebview2contextmenuitem.md) CreateContextMenuItem(string Label, [IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) iconStream, [CoreWebView2ContextMenuItemKind](corewebview2contextmenuitemkind.md) Kind)



### CreateCoreWebView2CompositionControllerAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;[CoreWebView2CompositionController](corewebview2compositioncontroller.md)&gt; CreateCoreWebView2CompositionControllerAsync([CoreWebView2ControllerWindowReference](corewebview2controllerwindowreference.md) ParentWindow)



### CreateCoreWebView2CompositionControllerAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;[CoreWebView2CompositionController](corewebview2compositioncontroller.md)&gt; CreateCoreWebView2CompositionControllerAsync([CoreWebView2ControllerWindowReference](corewebview2controllerwindowreference.md) ParentWindow, [CoreWebView2ControllerOptions](corewebview2controlleroptions.md) options)



### CreateCoreWebView2ControllerAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;[CoreWebView2Controller](corewebview2controller.md)&gt; CreateCoreWebView2ControllerAsync([CoreWebView2ControllerWindowReference](corewebview2controllerwindowreference.md) ParentWindow, [CoreWebView2ControllerOptions](corewebview2controlleroptions.md) options)



### CreateCoreWebView2ControllerAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;[CoreWebView2Controller](corewebview2controller.md)&gt; CreateCoreWebView2ControllerAsync([CoreWebView2ControllerWindowReference](corewebview2controllerwindowreference.md) ParentWindow)



### CreateCoreWebView2ControllerOptions

> [CoreWebView2ControllerOptions](corewebview2controlleroptions.md) CreateCoreWebView2ControllerOptions()



### CreateCoreWebView2PointerInfo

> [CoreWebView2PointerInfo](corewebview2pointerinfo.md) CreateCoreWebView2PointerInfo()



### CreatePrintSettings

> [CoreWebView2PrintSettings](corewebview2printsettings.md) CreatePrintSettings()



### CreateSharedBuffer

> [CoreWebView2SharedBuffer](corewebview2sharedbuffer.md) CreateSharedBuffer(uint64_t Size)



### CreateWebResourceRequest

> [CoreWebView2WebResourceRequest](corewebview2webresourcerequest.md) CreateWebResourceRequest(string uri, string Method, [IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) postData, string Headers)



### CreateWebResourceResponse

> [CoreWebView2WebResourceResponse](corewebview2webresourceresponse.md) CreateWebResourceResponse([IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) Content, int StatusCode, string ReasonPhrase, string Headers)



### CreateWithOptionsAsync

> static [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;CoreWebView2Environment&gt; CreateWithOptionsAsync(string browserExecutableFolder, string userDataFolder, [CoreWebView2EnvironmentOptions](corewebview2environmentoptions.md) options)



### GetAvailableBrowserVersionString

> static string GetAvailableBrowserVersionString()



### GetAvailableBrowserVersionString

> static string GetAvailableBrowserVersionString(string browserExecutableFolder)



### GetProcessInfos

> [`IVectorView`](/uwp/api/Windows.Foundation.Collections.IVectorView-1)&lt;[CoreWebView2ProcessInfo](corewebview2processinfo.md)&gt; GetProcessInfos()




## Events

### BrowserProcessExited

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2Environment, [CoreWebView2BrowserProcessExitedEventArgs](corewebview2browserprocessexitedeventargs.md)&gt;

### NewBrowserVersionAvailable

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2Environment, Object&gt;

### ProcessInfosChanged

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2Environment, Object&gt;



## Referenced by

- [CoreWebView2](corewebview2.md)
