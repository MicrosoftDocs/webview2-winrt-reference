---
title: CoreWebView2Environment
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/01/2024
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2Environment
---

# runtimeClass CoreWebView2Environment



## Summary

Members|Description
--|--
[BrowserVersionString](#browserversionstring) | 
[FailureReportFolderPath](#failurereportfolderpath) | 
[RenderAdapterLUID](#renderadapterluid) | 
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
[CreateTextureStream](#createtexturestream) | 
[CreateWebFileSystemDirectoryHandle](#createwebfilesystemdirectoryhandle) | 
[CreateWebFileSystemFileHandle](#createwebfilesystemfilehandle) | 
[CreateWebResourceRequest](#createwebresourcerequest) | 
[CreateWebResourceResponse](#createwebresourceresponse) | 
[CreateWithOptionsAsync](#createwithoptionsasync) | 
[GetAvailableBrowserVersionString](#getavailablebrowserversionstring) | 
[GetAvailableBrowserVersionString](#getavailablebrowserversionstring) | 
[GetAvailableBrowserVersionString](#getavailablebrowserversionstring) | 
[GetProcessExtendedInfosAsync](#getprocessextendedinfosasync) | 
[GetProcessInfos](#getprocessinfos) | 
[GetProcessInfosWithDetailsAsync](#getprocessinfoswithdetailsasync) | 
[UpdateRuntimeAsync](#updateruntimeasync) | 
[BrowserProcessExited](#browserprocessexited) | 
[NewBrowserVersionAvailable](#newbrowserversionavailable) | 
[ProcessInfosChanged](#processinfoschanged) | 
[RenderAdapterLUIDChanged](#renderadapterluidchanged) | 
[RestartRequested](#restartrequested) | 

## Properties

### BrowserVersionString

> readonly  string BrowserVersionString

### FailureReportFolderPath

> readonly  string FailureReportFolderPath

### RenderAdapterLUID

> readonly  uint64_t RenderAdapterLUID

### UserDataFolder

> readonly  string UserDataFolder



## Methods

### CompareBrowserVersionString

> static int CompareBrowserVersionString(string browserVersionString1, string browserVersionString2)



### CreateAsync

> static [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;[CoreWebView2Environment](corewebview2environment.md)&gt; CreateAsync()



### CreateContextMenuItem

> [CoreWebView2ContextMenuItem](corewebview2contextmenuitem.md) CreateContextMenuItem(string Label, [IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) iconStream, [CoreWebView2ContextMenuItemKind](corewebview2contextmenuitemkind.md) Kind)



### CreateCoreWebView2CompositionControllerAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;[CoreWebView2CompositionController](corewebview2compositioncontroller.md)&gt; CreateCoreWebView2CompositionControllerAsync([CoreWebView2ControllerWindowReference](corewebview2controllerwindowreference.md) operation)



### CreateCoreWebView2CompositionControllerAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;[CoreWebView2CompositionController](corewebview2compositioncontroller.md)&gt; CreateCoreWebView2CompositionControllerAsync([CoreWebView2ControllerWindowReference](corewebview2controllerwindowreference.md) operation, [CoreWebView2ControllerOptions](corewebview2controlleroptions.md) ParentWindow)



### CreateCoreWebView2ControllerAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;[CoreWebView2Controller](corewebview2controller.md)&gt; CreateCoreWebView2ControllerAsync([CoreWebView2ControllerWindowReference](corewebview2controllerwindowreference.md) operation, [CoreWebView2ControllerOptions](corewebview2controlleroptions.md) ParentWindow)



### CreateCoreWebView2ControllerAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;[CoreWebView2Controller](corewebview2controller.md)&gt; CreateCoreWebView2ControllerAsync([CoreWebView2ControllerWindowReference](corewebview2controllerwindowreference.md) operation)



### CreateCoreWebView2ControllerOptions

> [CoreWebView2ControllerOptions](corewebview2controlleroptions.md) CreateCoreWebView2ControllerOptions()



### CreateCoreWebView2PointerInfo

> [CoreWebView2PointerInfo](corewebview2pointerinfo.md) CreateCoreWebView2PointerInfo()



### CreatePrintSettings

> [CoreWebView2PrintSettings](corewebview2printsettings.md) CreatePrintSettings()



### CreateSharedBuffer

> [CoreWebView2SharedBuffer](corewebview2sharedbuffer.md) CreateSharedBuffer(uint64_t Size)



### CreateTextureStream

> [CoreWebView2TextureStream](corewebview2texturestream.md) CreateTextureStream(string streamId, Object d3dDevice)



### CreateWebFileSystemDirectoryHandle

> [CoreWebView2FileSystemHandle](corewebview2filesystemhandle.md) CreateWebFileSystemDirectoryHandle(string Path, [CoreWebView2FileSystemHandlePermission](corewebview2filesystemhandlepermission.md) Permission)



### CreateWebFileSystemFileHandle

> [CoreWebView2FileSystemHandle](corewebview2filesystemhandle.md) CreateWebFileSystemFileHandle(string Path, [CoreWebView2FileSystemHandlePermission](corewebview2filesystemhandlepermission.md) Permission)



### CreateWebResourceRequest

> [CoreWebView2WebResourceRequest](corewebview2webresourcerequest.md) CreateWebResourceRequest(string uri, string Method, [IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) postData, string Headers)



### CreateWebResourceResponse

> [CoreWebView2WebResourceResponse](corewebview2webresourceresponse.md) CreateWebResourceResponse([IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) Content, int StatusCode, string ReasonPhrase, string Headers)



### CreateWithOptionsAsync

> static [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;[CoreWebView2Environment](corewebview2environment.md)&gt; CreateWithOptionsAsync(string operation, string browserExecutableFolder, [CoreWebView2EnvironmentOptions](corewebview2environmentoptions.md) userDataFolder)



### GetAvailableBrowserVersionString

> static string GetAvailableBrowserVersionString(string browserExecutableFolder, [CoreWebView2EnvironmentOptions](corewebview2environmentoptions.md) options)



### GetAvailableBrowserVersionString

> static string GetAvailableBrowserVersionString()



### GetAvailableBrowserVersionString

> static string GetAvailableBrowserVersionString(string browserExecutableFolder)



### GetProcessExtendedInfosAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;[`IVectorView`](/uwp/api/Windows.Foundation.Collections.IVectorView-1)&lt;[CoreWebView2ProcessExtendedInfo](corewebview2processextendedinfo.md)&gt;&gt; GetProcessExtendedInfosAsync()



### GetProcessInfos

> [`IVectorView`](/uwp/api/Windows.Foundation.Collections.IVectorView-1)&lt;[CoreWebView2ProcessInfo](corewebview2processinfo.md)&gt; GetProcessInfos()



### GetProcessInfosWithDetailsAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;[`IVectorView`](/uwp/api/Windows.Foundation.Collections.IVectorView-1)&lt;[CoreWebView2ProcessInfo](corewebview2processinfo.md)&gt;&gt; GetProcessInfosWithDetailsAsync()



### UpdateRuntimeAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;[CoreWebView2UpdateRuntimeResult](corewebview2updateruntimeresult.md)&gt; UpdateRuntimeAsync()




## Events

### BrowserProcessExited

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2Environment](corewebview2environment.md), [CoreWebView2BrowserProcessExitedEventArgs](corewebview2browserprocessexitedeventargs.md)&gt;

### NewBrowserVersionAvailable

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2Environment](corewebview2environment.md), Object&gt;

### ProcessInfosChanged

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2Environment](corewebview2environment.md), Object&gt;

### RenderAdapterLUIDChanged

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2Environment](corewebview2environment.md), Object&gt;

### RestartRequested

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2Environment](corewebview2environment.md), [CoreWebView2RestartRequestedEventArgs](corewebview2restartrequestedeventargs.md)&gt;



## Referenced by

- [CoreWebView2](corewebview2.md)
