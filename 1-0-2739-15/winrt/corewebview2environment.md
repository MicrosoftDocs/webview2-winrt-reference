---
description: This represents the WebView2 Environment.
title: CoreWebView2Environment
ms.date: 08/26/2024
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
- Microsoft.Web.WebView2.Core.CoreWebView2Environment.CreateWebFileSystemDirectoryHandle
- Microsoft.Web.WebView2.Core.CoreWebView2Environment.CreateWebFileSystemFileHandle
- Microsoft.Web.WebView2.Core.CoreWebView2Environment.CreateWebResourceRequest
- Microsoft.Web.WebView2.Core.CoreWebView2Environment.CreateWebResourceResponse
- Microsoft.Web.WebView2.Core.CoreWebView2Environment.CreateWithOptionsAsync
- Microsoft.Web.WebView2.Core.CoreWebView2Environment.GetAvailableBrowserVersionString
- Microsoft.Web.WebView2.Core.CoreWebView2Environment.GetAvailableBrowserVersionString
- Microsoft.Web.WebView2.Core.CoreWebView2Environment.GetAvailableBrowserVersionString
- Microsoft.Web.WebView2.Core.CoreWebView2Environment.GetProcessExtendedInfosAsync
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



This represents the WebView2 Environment.
WebViews created from an environment run on the Browser process specified with environment parameters and objects created from an environment should be used in the same environment. Using it in different environments are not guaranteed to be compatible and may fail.

## Summary

Members|Description
--|--
[BrowserVersionString](#browserversionstring) | Gets the browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.
[FailureReportFolderPath](#failurereportfolderpath) | Gets the failure report folder that all CoreWebView2s created from this environment are using.
[UserDataFolder](#userdatafolder) | Gets the user data folder that all CoreWebView2s created from this environment are using.
[CompareBrowserVersionString](#comparebrowserversionstring) | Compares two instances of browser versions correctly and returns an integer that indicates whether the first instance is older, the same as, or newer than the second instance.
[CreateAsync](#createasync) | Creates a WebView2 Environment using the installed or a custom WebView2 Runtime version.
[CreateContextMenuItem](#createcontextmenuitem) | Create a custom [CoreWebView2ContextMenuItem](corewebview2contextmenuitem.md) object to insert into the WebView context menu.
[CreateCoreWebView2CompositionControllerAsync](#createcorewebview2compositioncontrollerasync) | Asynchronously creates a new WebView for use with visual hosting.
[CreateCoreWebView2CompositionControllerAsync](#createcorewebview2compositioncontrollerasync) | This is a overload method that creates a WebView2 composition controller using parent window and custom controller options.
[CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync) | This is a overload method that creates a WebView2 controller using parent window and custom controller options.
[CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync) | Asynchronously creates a new WebView.
[CreateCoreWebView2ControllerOptions](#createcorewebview2controlleroptions) | This is a overload method that creates a WebView2 ControllerOptions.
[CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo) | Creates an empty [CoreWebView2PointerInfo](corewebview2pointerinfo.md).
[CreatePrintSettings](#createprintsettings) | Creates the [CoreWebView2PrintSettings](corewebview2printsettings.md) used by the [CoreWebView2.PrintToPdfAsync](corewebview2.md#printtopdfasync) method.
[CreateSharedBuffer](#createsharedbuffer) | Create a shared memory based buffer with the specified size in bytes.
[CreateWebFileSystemDirectoryHandle](#createwebfilesystemdirectoryhandle) | Creates a [CoreWebView2FileSystemHandle](corewebview2filesystemhandle.md) object from a path that represents a Web [FileSystemDirectoryHandle](https://developer.mozilla.org/docs/Web/API/FileSystemDirectoryHandle).
[CreateWebFileSystemFileHandle](#createwebfilesystemfilehandle) | Creates a [CoreWebView2FileSystemHandle](corewebview2filesystemhandle.md) object from a path that represents a Web [FileSystemFileHandle](https://developer.mozilla.org/docs/Web/API/FileSystemFileHandle).
[CreateWebResourceRequest](#createwebresourcerequest) | Creates a new [CoreWebView2WebResourceRequest](corewebview2webresourcerequest.md) object.
[CreateWebResourceResponse](#createwebresourceresponse) | Creates a new [CoreWebView2WebResourceResponse](corewebview2webresourceresponse.md) object.
[CreateWithOptionsAsync](#createwithoptionsasync) | Creates a WebView2 Environment with a custom version of WebView2 Runtime, user data folder, and environment options.
[GetAvailableBrowserVersionString](#getavailablebrowserversionstring) | Gets the browser version info including channel name if it is not the stable channel or WebView2 Runtime where `browserExecutableFolder` is the relative path to the folder that contains the WebView2 Runtime and `options` is the CoreWebViewEnvironmentOptions object used to create the environment.
[GetAvailableBrowserVersionString](#getavailablebrowserversionstring) | Gets the browser version info including channel name if it is not the stable channel or WebView2 Runtime.
[GetAvailableBrowserVersionString](#getavailablebrowserversionstring) | Gets the browser version info including channel name if it is not the stable channel or WebView2 Runtime where `browserExecutableFolder` is the relative path to the folder that contains the WebView2 Runtime.
[GetProcessExtendedInfosAsync](#getprocessextendedinfosasync) | Returns a snapshot collection of [CoreWebView2ProcessInfo](corewebview2processinfo.md) corresponding to all currently running processes associated with this CoreWebView2Environment excludes crashpad process. This provides the same list of [CoreWebView2ProcessInfo](corewebview2processinfo.md) as what's provided in [CoreWebView2Environment.GetProcessInfos](corewebview2environment.md#getprocessinfos), but additionally provides a list of associated [CoreWebView2FrameInfo](corewebview2frameinfo.md) which are actively running (showing or hiding UI elements) in the renderer process. See [CoreWebView2ProcessExtendedInfo.AssociatedFrameInfos](corewebview2processextendedinfo.md#associatedframeinfos) for more information.
[GetProcessInfos](#getprocessinfos) | Returns the list of all [CoreWebView2ProcessInfo](corewebview2processinfo.md) using same user data folder except for crashpad process.
[BrowserProcessExited](#browserprocessexited) | BrowserProcessExited is raised when the collection of WebView2 Runtime processes for the browser process of this CoreWebView2Environment terminate due to browser process failure or normal shutdown (for example, when all associated WebViews are closed), after all resources have been released (including the user data folder).
[NewBrowserVersionAvailable](#newbrowserversionavailable) | NewBrowserVersionAvailable is raised when a newer version of the WebView2 Runtime is installed and available using WebView2.
[ProcessInfosChanged](#processinfoschanged) | ProcessInfosChanged is raised when a collection of WebView2 Runtime processes changed due to new process being detected or when a existing process gone away.

## Properties

### BrowserVersionString

> readonly  string BrowserVersionString

Gets the browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.
It matches the format of the [CoreWebView2Environment.GetAvailableBrowserVersionString](corewebview2environment.md#getavailablebrowserversionstring) method. Channel names are `beta`, `dev`, and `canary`.

### FailureReportFolderPath

> readonly  string FailureReportFolderPath

Gets the failure report folder that all CoreWebView2s created from this environment are using.

### UserDataFolder

> readonly  string UserDataFolder

Gets the user data folder that all CoreWebView2s created from this environment are using.
This could be either the value passed in by the developer when creating the environment object or the calculated one for default handling. And will always be an absolute path.



## Methods

### CompareBrowserVersionString

> static int CompareBrowserVersionString(string browserVersionString1, string browserVersionString2)

Compares two instances of browser versions correctly and returns an integer that indicates whether the first instance is older, the same as, or newer than the second instance.
`browserVersionString1` is one of the version strings to compare. `browserVersionString2` is the other version string to compare.



### CreateAsync

> static [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;CoreWebView2Environment&gt; CreateAsync()

Creates a WebView2 Environment using the installed or a custom WebView2 Runtime version.



### CreateContextMenuItem

> [CoreWebView2ContextMenuItem](corewebview2contextmenuitem.md) CreateContextMenuItem(string Label, [IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) iconStream, [CoreWebView2ContextMenuItemKind](corewebview2contextmenuitemkind.md) Kind)

Create a custom [CoreWebView2ContextMenuItem](corewebview2contextmenuitem.md) object to insert into the WebView context menu.
CoreWebView2 will rewind the `icon` stream before decoding.
There is a limit of 1000 active custom context menu items at a given time per CoreWebView2Environment. Attempting to create more before deleting existing ones will fail with `ERROR_NOT_ENOUGH_QUOTA`. It is recommended to reuse custom ContextMenuItems across CoreWebView2ContextMenuRequested events for performance. The created object's [CoreWebView2ContextMenuItem.IsEnabled](corewebview2contextmenuitem.md#isenabled) property will default to `true` and [CoreWebView2ContextMenuItem.IsChecked](corewebview2contextmenuitem.md#ischecked) property will default to `false`. A [CoreWebView2ContextMenuItem.CommandId](corewebview2contextmenuitem.md#commandid) will be assigned that's unique across active custom context menu items, but command ID values of deleted custom ContextMenuItems can be reassigned.



### CreateCoreWebView2CompositionControllerAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;[CoreWebView2CompositionController](corewebview2compositioncontroller.md)&gt; CreateCoreWebView2CompositionControllerAsync([CoreWebView2ControllerWindowReference](corewebview2controllerwindowreference.md) ParentWindow)

Asynchronously creates a new WebView for use with visual hosting.
`ParentWindow` will be the HWND that the app will receive pointer/mouse input meant for the WebView (and will need to use [CoreWebView2CompositionController.SendMouseInput](corewebview2compositioncontroller.md#sendmouseinput) or [CoreWebView2CompositionController.SendPointerInput](corewebview2compositioncontroller.md#sendpointerinput) to forward). If the app moves the WebView visual tree to underneath a different window, then it needs to set [CoreWebView2Controller.ParentWindow](corewebview2controller.md#parentwindow) to update the new parent HWND of the visual tree.

Set [CoreWebView2CompositionController.RootVisualTarget](corewebview2compositioncontroller.md#rootvisualtarget) property on the created [CoreWebView2CompositionController](corewebview2compositioncontroller.md) to provide a visual to host the browser's visual tree.

It is recommended that the application set Application User Model ID for the process or the application window. If none is set, during WebView creation a generated Application User Model ID is set to root window of `ParentWindow`.

It can also accept a [CoreWebView2ControllerOptions](corewebview2controlleroptions.md) which is created by [CoreWebView2Environment.CreateCoreWebView2ControllerOptions](corewebview2environment.md#createcorewebview2controlleroptions) as the second parameter for multiple profiles support.

CreateCoreWebView2CompositionController is supported in the following versions of Windows:

- Windows 11
- Windows 10
- Windows Server 2019
- Windows Server 2016



### CreateCoreWebView2CompositionControllerAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;[CoreWebView2CompositionController](corewebview2compositioncontroller.md)&gt; CreateCoreWebView2CompositionControllerAsync([CoreWebView2ControllerWindowReference](corewebview2controllerwindowreference.md) ParentWindow, [CoreWebView2ControllerOptions](corewebview2controlleroptions.md) options)

This is a overload method that creates a WebView2 composition controller using parent window and custom controller options.



### CreateCoreWebView2ControllerAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;[CoreWebView2Controller](corewebview2controller.md)&gt; CreateCoreWebView2ControllerAsync([CoreWebView2ControllerWindowReference](corewebview2controllerwindowreference.md) ParentWindow, [CoreWebView2ControllerOptions](corewebview2controlleroptions.md) options)

This is a overload method that creates a WebView2 controller using parent window and custom controller options.



### CreateCoreWebView2ControllerAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;[CoreWebView2Controller](corewebview2controller.md)&gt; CreateCoreWebView2ControllerAsync([CoreWebView2ControllerWindowReference](corewebview2controllerwindowreference.md) ParentWindow)

Asynchronously creates a new WebView.
The WebView adds a child window to the provided window during WebView creation. Z-order and other things impacted by sibling window order are affected accordingly.

HWND_MESSAGE is a valid parameter for `ParentWindow` for an invisible WebView for Windows 8 and above. In this case the window will never become visible. You are not able to reparent the window after you have created the WebView. This is not supported in Windows 7 or below. Passing this parameter in Windows 7 or below will return ERROR_INVALID_WINDOW_HANDLE in the controller callback.

It can also accept a [CoreWebView2ControllerOptions](corewebview2controlleroptions.md) which is created by [CoreWebView2Environment.CreateCoreWebView2ControllerOptions](corewebview2environment.md#createcorewebview2controlleroptions) as the second parameter for multiple profiles support. As WebView2 is built on top of Edge browser, it follows Edge's behavior pattern. To create an InPrivate WebView, we gets an off-the-record profile (an InPrivate profile) from a regular profile, then create the WebView with the off-the-record profile. Multiple profiles under single user data directory can share some system resources including memory, CPU footprint, disk space (such as compiled shaders and safebrowsing data) etc.

It is recommended that the application set Application User Model ID for the process or the application window. If none is set, during WebView creation a generated Application User Model ID is set to root window of `ParentWindow`.

It is recommended that the app handles restart manager messages, to gracefully restart it in the case when the app is using the WebView2 Runtime from a certain installation and that installation is being uninstalled. For example, if a user installs a version of the WebView2 Runtime and opts to use another version of the WebView2 Runtime for testing the app, and then uninstalls the 1st version of the WebView2 Runtime without closing the app, the app restarts to allow un-installation to succeed.

When the app retries CreateCoreWebView2ControllerAsync upon failure, it is recommended that the app restarts from creating a new WebView2 Environment. If a WebView2 Runtime update happens, the version associated with a WebView2 Environment may have been removed and causing the object to no longer work. Creating a new WebView2 Environment works since it uses the latest version.

WebView creation fails if a running instance using the same user data folder exists, and the Environment objects have different [CoreWebView2EnvironmentOptions](corewebview2environmentoptions.md). For example, if a WebView was created with one [CoreWebView2EnvironmentOptions.Language](corewebview2environmentoptions.md#language), an attempt to create a WebView with a different [CoreWebView2EnvironmentOptions.Language](corewebview2environmentoptions.md#language) using the same user data folder fails.

WebView creation can fail with `E_UNEXPECTED` if runtime does not have permissions to the user data folder.



### CreateCoreWebView2ControllerOptions

> [CoreWebView2ControllerOptions](corewebview2controlleroptions.md) CreateCoreWebView2ControllerOptions()

This is a overload method that creates a WebView2 ControllerOptions.



### CreateCoreWebView2PointerInfo

> [CoreWebView2PointerInfo](corewebview2pointerinfo.md) CreateCoreWebView2PointerInfo()

Creates an empty [CoreWebView2PointerInfo](corewebview2pointerinfo.md).
The returned [CoreWebView2PointerInfo](corewebview2pointerinfo.md) needs to be populated with all of the relevant info before calling [CoreWebView2CompositionController.SendPointerInput](corewebview2compositioncontroller.md#sendpointerinput).



### CreatePrintSettings

> [CoreWebView2PrintSettings](corewebview2printsettings.md) CreatePrintSettings()

Creates the [CoreWebView2PrintSettings](corewebview2printsettings.md) used by the [CoreWebView2.PrintToPdfAsync](corewebview2.md#printtopdfasync) method.



### CreateSharedBuffer

> [CoreWebView2SharedBuffer](corewebview2sharedbuffer.md) CreateSharedBuffer(uint64_t Size)

Create a shared memory based buffer with the specified size in bytes.
The buffer can be shared with web contents in WebView by calling [CoreWebView2.PostSharedBufferToScript](corewebview2.md#postsharedbuffertoscript) or [CoreWebView2Frame.PostSharedBufferToScript](corewebview2frame.md#postsharedbuffertoscript).
Once shared, the same content of the buffer will be accessible from both the app process and script in WebView.
Modification to the content will be visible to all parties that have access to the buffer.
The shared buffer is presented to the script as ArrayBuffer. All JavaScript APIs that work for ArrayBuffer including Atomics APIs can be used on it.
There is currently a limitation that only size less than 2GB is supported.



### CreateWebFileSystemDirectoryHandle

> [CoreWebView2FileSystemHandle](corewebview2filesystemhandle.md) CreateWebFileSystemDirectoryHandle(string Path, [CoreWebView2FileSystemHandlePermission](corewebview2filesystemhandlepermission.md) Permission)

Creates a [CoreWebView2FileSystemHandle](corewebview2filesystemhandle.md) object from a path that represents a Web [FileSystemDirectoryHandle](https://developer.mozilla.org/docs/Web/API/FileSystemDirectoryHandle).
This must be a syntactically correct fully qualified path, but it is not checked here whether it currently points to a directory. Any other state validation will be done when this handle is accessed from web content and will cause DOM exceptions if access operations fail. If an invalid path is passed, an `InvalidArgumentException` will be thrown.
Note: An exception to this is, if there is a parent directory handle that has broader permissions in the same page context than specified in here, the handle will automatically inherit the most permissive permission of the parent handle when posted to that page context. i.e. If there is already a `FileSystemDirectoryHandle` to `C:\foo` that has write permission on a page, even though a [CoreWebView2FileSystemHandle](corewebview2filesystemhandle.md) to directory `C:\example\directory` may be created with [CoreWebView2FileSystemHandlePermission.ReadOnly](corewebview2filesystemhandlepermission.md#readonly) permission, when posted to that page, write permission will be automatically granted to the created handle.
Additionally, the app must have the same OS permissions that have propagated to the [WebView2 browser process](/microsoft-edge/webview2/concepts/process-model) for the path it wishes to give the web content to make any operations on the directory. Specifically, the WebView2 browser process will run in same user, package identity, and app container of the app, but other means such as security context impersonations do not get propagated, so such permissions that the app has, will not be effective in WebView2.
An app needs to be mindful that this object, when posted to the web content, provides it with unusual access to OS file system via the Web FileSystem API! The app should therefore only post objects for paths that it wants to allow access to the web content and it is not recommended that the web content "asks" for this path. The app should also check the source property of the target to ensure that it is sending to the web content of intended origin. Once the object is passed to web content, the path must point to a directory as if it was chosen via [directory picker](https://developer.mozilla.org/docs/Web/API/Window/showDirectoryPicker) otherwise any IO operation done on the `FileSystemDirectoryHandle` will throw a DOM exception.



### CreateWebFileSystemFileHandle

> [CoreWebView2FileSystemHandle](corewebview2filesystemhandle.md) CreateWebFileSystemFileHandle(string Path, [CoreWebView2FileSystemHandlePermission](corewebview2filesystemhandlepermission.md) Permission)

Creates a [CoreWebView2FileSystemHandle](corewebview2filesystemhandle.md) object from a path that represents a Web [FileSystemFileHandle](https://developer.mozilla.org/docs/Web/API/FileSystemFileHandle).
Note: An exception to this is, if there is a parent directory handle that has broader permissions in the same page context than specified in here, the handle will automatically inherit the most permissive permission of the parent handle when posted to that page context. i.e. If there is already a `FileSystemDirectoryHandle` to `C:\foo` that has write permission on a page, even though a [CoreWebView2FileSystemHandle](corewebview2filesystemhandle.md) to file `C:\example\file.txt` may be created with [CoreWebView2FileSystemHandlePermission.ReadOnly](corewebview2filesystemhandlepermission.md#readonly) permission, when posted to that page, write permission will be automatically granted to the created handle.
Additionally, the app must have the same OS permissions that have propagated to the [WebView2 browser process](/microsoft-edge/webview2/concepts/process-model) for the path it wishes to give the web content to read/write the file. Specifically, the WebView2 browser process will run in same user, package identity, and app container of the app, but other means such as security context impersonations do not get propagated, so such permissions that the app has, will not be effective in WebView2.
An app needs to be mindful that this object, when posted to the web content, provides it with unusual access to OS file system via the Web FileSystem API! The app should therefore only post objects for paths that it wants to allow access to the web content and it is not recommended that the web content "asks" for this path. The app should also check the source property of the target to ensure that it is sending to the web content of intended origin. Once the object is passed to web content, if the content is attempting a read, the file must be existing and available to read similar to a file chosen by [open file picker](https://developer.mozilla.org/docs/Web/API/Window/showOpenFilePicker), otherwise the read operation will [throw a DOM exception](https://developer.mozilla.org/docs/Web/API/FileSystemFileHandle/getFile#exceptions). For write operations, the file does not need to exist as `FileSystemFileHandle` will behave as a file path chosen by [save file picker](https://developer.mozilla.org/docs/Web/API/Window/showSaveFilePicker) and will create or overwrite the file, but the parent directory structure pointed by the file must exist and an existing file must be available to write and delete or the write operation will [throw a DOM exception](https://developer.mozilla.org/docs/Web/API/FileSystemFileHandle/createWritable#exceptions).



### CreateWebResourceRequest

> [CoreWebView2WebResourceRequest](corewebview2webresourcerequest.md) CreateWebResourceRequest(string uri, string Method, [IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) postData, string Headers)

Creates a new [CoreWebView2WebResourceRequest](corewebview2webresourcerequest.md) object.
`uri` parameter must be absolute URI. It's also possible to create this object with `null` headers string and then use the [CoreWebView2HttpRequestHeaders](corewebview2httprequestheaders.md) to construct the headers line by line.



### CreateWebResourceResponse

> [CoreWebView2WebResourceResponse](corewebview2webresourceresponse.md) CreateWebResourceResponse([IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) Content, int StatusCode, string ReasonPhrase, string Headers)

Creates a new [CoreWebView2WebResourceResponse](corewebview2webresourceresponse.md) object.
It is also possible to create this object with empty headers string and then use the [CoreWebView2HttpResponseHeaders](corewebview2httpresponseheaders.md) to construct the headers line by line.



### CreateWithOptionsAsync

> static [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;CoreWebView2Environment&gt; CreateWithOptionsAsync(string browserExecutableFolder, string userDataFolder, [CoreWebView2EnvironmentOptions](corewebview2environmentoptions.md) options)

Creates a WebView2 Environment with a custom version of WebView2 Runtime, user data folder, and environment options.



### GetAvailableBrowserVersionString

> static string GetAvailableBrowserVersionString(string browserExecutableFolder, [CoreWebView2EnvironmentOptions](corewebview2environmentoptions.md) options)

Gets the browser version info including channel name if it is not the stable channel or WebView2 Runtime where `browserExecutableFolder` is the relative path to the folder that contains the WebView2 Runtime and `options` is the CoreWebViewEnvironmentOptions object used to create the environment.



### GetAvailableBrowserVersionString

> static string GetAvailableBrowserVersionString()

Gets the browser version info including channel name if it is not the stable channel or WebView2 Runtime.



### GetAvailableBrowserVersionString

> static string GetAvailableBrowserVersionString(string browserExecutableFolder)

Gets the browser version info including channel name if it is not the stable channel or WebView2 Runtime where `browserExecutableFolder` is the relative path to the folder that contains the WebView2 Runtime.



### GetProcessExtendedInfosAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;[`IVectorView`](/uwp/api/Windows.Foundation.Collections.IVectorView-1)&lt;[CoreWebView2ProcessExtendedInfo](corewebview2processextendedinfo.md)&gt;&gt; GetProcessExtendedInfosAsync()

Returns a snapshot collection of [CoreWebView2ProcessInfo](corewebview2processinfo.md) corresponding to all currently running processes associated with this CoreWebView2Environment excludes crashpad process. This provides the same list of [CoreWebView2ProcessInfo](corewebview2processinfo.md) as what's provided in [CoreWebView2Environment.GetProcessInfos](corewebview2environment.md#getprocessinfos), but additionally provides a list of associated [CoreWebView2FrameInfo](corewebview2frameinfo.md) which are actively running (showing or hiding UI elements) in the renderer process. See [CoreWebView2ProcessExtendedInfo.AssociatedFrameInfos](corewebview2processextendedinfo.md#associatedframeinfos) for more information.



### GetProcessInfos

> [`IVectorView`](/uwp/api/Windows.Foundation.Collections.IVectorView-1)&lt;[CoreWebView2ProcessInfo](corewebview2processinfo.md)&gt; GetProcessInfos()

Returns the list of all [CoreWebView2ProcessInfo](corewebview2processinfo.md) using same user data folder except for crashpad process.




## Events

### BrowserProcessExited

BrowserProcessExited is raised when the collection of WebView2 Runtime processes for the browser process of this CoreWebView2Environment terminate due to browser process failure or normal shutdown (for example, when all associated WebViews are closed), after all resources have been released (including the user data folder).
Multiple app processes can share a browser process by creating their webviews from a CoreWebView2Environment with the same user data folder. When the entire collection of WebView2Runtime processes for the browser process exit, all associated CoreWebView2Environment objects receive the BrowserProcessExited event. Multiple processes sharing the same browser process need to coordinate their use of the shared user data folder to avoid race conditions and unnecessary waits. For example, one process should not clear the user data folder at the same time that another process recovers from a crash by recreating its WebView controls; one process should not block waiting for the event if other app processes are using the same browser process (the browser process will not exit until those other processes have closed their webviews too).

Note this is an event from CoreWebView2Environment, not [CoreWebView2](corewebview2.md). The difference between BrowserProcessExited and [CoreWebView2.ProcessFailed](corewebview2.md#processfailed) is that BrowserProcessExited is raised for any **browser process** exit (expected or unexpected, after all associated processes have exited too), while [CoreWebView2.ProcessFailed](corewebview2.md#processfailed) is raised for **unexpected** process exits of any kind (browser, render, GPU, and all other types), or for main frame **render process** unresponsiveness. To learn more about the WebView2 Process Model, go to [Process model](/microsoft-edge/webview2/concepts/process-model).

In the case the browser process crashes, both BrowserProcessExited and [CoreWebView2.ProcessFailed](corewebview2.md#processfailed) events are raised, but the order is not guaranteed. These events are intended for different scenarios. It is up to the app to coordinate the handlers so they do not try to perform reliability recovery while also trying to move to a new WebView2 Runtime version or remove the user data folder.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2Environment, [CoreWebView2BrowserProcessExitedEventArgs](corewebview2browserprocessexitedeventargs.md)&gt;

### NewBrowserVersionAvailable

NewBrowserVersionAvailable is raised when a newer version of the WebView2 Runtime is installed and available using WebView2.
To use the newer version of the browser you must create a new environment and WebView. The event is only raised for new version from the same WebView2 Runtime from which the code is running. When not running with installed WebView2 Runtime, no event is raised.

Because a user data folder is only able to be used by one browser process at a time, if you want to use the same user data folder in the WebViews using the new version of the browser, you must close the environment and instance of WebView that are using the older version of the browser first. Or simply prompt the user to restart the app.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2Environment, Object&gt;

### ProcessInfosChanged

ProcessInfosChanged is raised when a collection of WebView2 Runtime processes changed due to new process being detected or when a existing process gone away.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2Environment, Object&gt;



## Referenced by

- [CoreWebView2](corewebview2.md)
