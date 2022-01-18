---
description: This represents the WebView2 Environment.
title: CoreWebView2Environment
ms.date: 01/18/2022
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2Environment
---

# CoreWebView2Environment Class



This represents the WebView2 Environment.
WebViews created from an environment run on the Browser process specified with environment parameters and objects created from an environment should be used in the same environment. Using it in different environments are not guaranteed to be compatible and may fail.

## Summary

Members|Description
--|--
[BrowserVersionString](#browserversionstring) | Gets the browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.
[UserDataFolder](#userdatafolder) | Gets the user data folder that all CoreWebView2s created from this environment are using.
[CompareBrowserVersionString](#comparebrowserversionstring) | Compares two instances of browser versions correctly and returns an integer that indicates whether the first instance is older, the same as, or newer than the second instance.
[CreateAsync](#createasync) | Creates a WebView2 Environment using the installed or a custom WebView2 Runtime version.
[CreateContextMenuItem](#createcontextmenuitem) | Create a [CoreWebView2ContextMenuItem](corewebview2contextmenuitem.md) object to insert into the WebView context menu.
[CreateCoreWebView2CompositionControllerAsync](#createcorewebview2compositioncontrollerasync) | Asynchronously creates a new WebView for use with visual hosting.
[CreateCoreWebView2CompositionControllerWithOptionsAsync](#createcorewebview2compositioncontrollerwithoptionsasync) | Create a new webview in visual hosting mode with [CoreWebView2ControllerOptions](corewebview2controlleroptions.md) as parameter for multiple profiles support.
[CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync) | Asynchronously creates a new WebView.
[CreateCoreWebView2ControllerOptions](#createcorewebview2controlleroptions) | Create a new [CoreWebView2ControllerOptions](corewebview2controlleroptions.md) object, which can be passed as a parameter in [CoreWebView2Environment.CreateCoreWebView2ControllerWithOptionsAsync](corewebview2environment.md#createcorewebview2controllerwithoptionsasync) and [CoreWebView2Environment.CreateCoreWebView2CompositionControllerWithOptionsAsync](corewebview2environment.md#createcorewebview2compositioncontrollerwithoptionsasync) function for multiple profiles support.
[CreateCoreWebView2ControllerWithOptionsAsync](#createcorewebview2controllerwithoptionsasync) | Create a new webview with [CoreWebView2ControllerOptions](corewebview2controlleroptions.md) as parameter for multiple profiles support.
[CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo) | Creates an empty [CoreWebView2PointerInfo](corewebview2pointerinfo.md).
[CreatePrintSettings](#createprintsettings) | Creates the [CoreWebView2PrintSettings](corewebview2printsettings.md) used by the [CoreWebView2.PrintToPdfAsync](corewebview2.md#printtopdfasync) method.
[CreateWebResourceRequest](#createwebresourcerequest) | Creates a new [CoreWebView2WebResourceRequest](corewebview2webresourcerequest.md) object.
[CreateWebResourceResponse](#createwebresourceresponse) | Creates a new [CoreWebView2WebResourceResponse](corewebview2webresourceresponse.md) object.
[CreateWithOptionsAsync](#createwithoptionsasync) | Creates a WebView2 Environment with a custom version of WebView2 Runtime, user data folder, and environment options.
[GetAvailableBrowserVersionString](#getavailablebrowserversionstring) | Gets the browser version info including channel name if it is not the stable channel or WebView2 Runtime.
[GetAvailableBrowserVersionString](#getavailablebrowserversionstring) | Gets the browser version info including channel name if it is not the stable channel or WebView2 Runtime where `browserExecutableFolder` is the relative path to the folder that contains the WebView2 Runtime.
[GetProcessInfos](#getprocessinfos) | Returns the list of [CoreWebView2ProcessInfo](corewebview2processinfo.md).
[UpdateRuntimeAsync](#updateruntimeasync) | Try to update the installed Microsoft Edge WebView2 Runtime.
[BrowserProcessExited](#browserprocessexited) | BrowserProcessExited is raised when the collection of WebView2 Runtime processes for the browser process of this CoreWebView2Environment terminate due to browser process failure or normal shutdown (for example, when all associated WebViews are closed), after all resources have been released (including the user data folder).
[NewBrowserVersionAvailable](#newbrowserversionavailable) | NewBrowserVersionAvailable is raised when a newer version of the WebView2 Runtime is installed and available using WebView2.
[ProcessInfosChanged](#processinfoschanged) | ProcessInfosChanged is raised when a collection of WebView2 Runtime processes changed due to new process being detected or when a existing process gone away.

## Properties

### BrowserVersionString

> readonly  string BrowserVersionString

Gets the browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.
It matches the format of the [CoreWebView2Environment.GetAvailableBrowserVersionString](corewebview2environment.md#getavailablebrowserversionstring) method. Channel names are `beta`, `dev`, and `canary`.

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

Create a [CoreWebView2ContextMenuItem](corewebview2contextmenuitem.md) object to insert into the WebView context menu.
CoreWebView2 will rewind the `icon` stream before decoding.
[CoreWebView2ContextMenuItem.CommandId](corewebview2contextmenuitem.md#commandid) for new custom menu items will be unique for the lifespan of the ContextMenuRequested event. There is currently a limit of 1000 context menu items that can be created per CoreWebView2Environment. The specific command ID values may change from build to build so do not rely on the actual value, but instead use the value given from the object `CommandId` instead. The returned `CoreWebView2ContextMenuItem` object's [CoreWebView2ContextMenuItem.IsEnabled](corewebview2contextmenuitem.md#isenabled) property will default to `true` and [CoreWebView2ContextMenuItem.IsChecked](corewebview2contextmenuitem.md#ischecked) property will default to `false`.



### CreateCoreWebView2CompositionControllerAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;[CoreWebView2CompositionController](corewebview2compositioncontroller.md)&gt; CreateCoreWebView2CompositionControllerAsync([CoreWebView2ControllerWindowReference](corewebview2controllerwindowreference.md) ParentWindow)

Asynchronously creates a new WebView for use with visual hosting.
`ParentWindow` will be the HWND that the app will receive pointer/mouse input meant for the WebView (and will need to use [CoreWebView2CompositionController.SendMouseInput](corewebview2compositioncontroller.md#sendmouseinput) or [CoreWebView2CompositionController.SendPointerInput](corewebview2compositioncontroller.md#sendpointerinput) to forward). If the app moves the WebView visual tree to underneath a different window, then it needs to set [CoreWebView2Controller.ParentWindow](corewebview2controller.md#parentwindow) to update the new parent HWND of the visual tree.

Set [CoreWebView2CompositionController.RootVisualTarget](corewebview2compositioncontroller.md#rootvisualtarget) property on the created [CoreWebView2CompositionController](corewebview2compositioncontroller.md) to provide a visual to host the browser's visual tree.

It is recommended that the application set Application User Model ID for the process or the application window. If none is set, during WebView creation a generated Application User Model ID is set to root window of `ParentWindow`.

CreateCoreWebView2Controller is supported in the following versions of Windows:

- Windows 11
- Windows 10
- Windows Server 2019
- Windows Server 2016




### CreateCoreWebView2CompositionControllerWithOptionsAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;[CoreWebView2CompositionController](corewebview2compositioncontroller.md)&gt; CreateCoreWebView2CompositionControllerWithOptionsAsync([CoreWebView2ControllerWindowReference](corewebview2controllerwindowreference.md) ParentWindow, [CoreWebView2ControllerOptions](corewebview2controlleroptions.md) options)

Create a new webview in visual hosting mode with [CoreWebView2ControllerOptions](corewebview2controlleroptions.md) as parameter for multiple profiles support.
If a new webview has been created, the IAsyncOperation will be immediately invoked.



### CreateCoreWebView2ControllerAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;[CoreWebView2Controller](corewebview2controller.md)&gt; CreateCoreWebView2ControllerAsync([CoreWebView2ControllerWindowReference](corewebview2controllerwindowreference.md) ParentWindow)

Asynchronously creates a new WebView.
The WebView adds a child window to the provided window during WebView creation. Z-order and other things impacted by sibling window order are affected accordingly.

It is recommended that the application set Application User Model ID for the process or the application window. If none is set, during WebView creation a generated Application User Model ID is set to root window of `ParentWindow`.

It is recommended that the app handles restart manager messages, to gracefully restart it in the case when the app is using the WebView2 Runtime from a certain installation and that installation is being uninstalled. For example, if a user installs a version of the WebView2 Runtime and opts to use another version of the WebView2 Runtime for testing the app, and then uninstalls the 1st version of the WebView2 Runtime without closing the app, the app restarts to allow un-installation to succeed.

When the app retries CreateCoreWebView2ControllerAsync upon failure, it is recommended that the app restarts from creating a new WebView2 Environment. If a WebView2 Runtime update happens, the version associated with a WebView2 Environment may have been removed and causing the object to no longer work. Creating a new WebView2 Environment works since it uses the latest version.

WebView creation fails if a running instance using the same user data folder exists, and the Environment objects have different [CoreWebView2EnvironmentOptions](corewebview2environmentoptions.md). For example, if a WebView was created with one [CoreWebView2EnvironmentOptions.Language](corewebview2environmentoptions.md#language), an attempt to create a WebView with a different [CoreWebView2EnvironmentOptions.Language](corewebview2environmentoptions.md#language) using the same user data folder fails.



### CreateCoreWebView2ControllerOptions

> [CoreWebView2ControllerOptions](corewebview2controlleroptions.md) CreateCoreWebView2ControllerOptions(string ProfileName, int IsInPrivateModeEnabled)

Create a new [CoreWebView2ControllerOptions](corewebview2controlleroptions.md) object, which can be passed as a parameter in [CoreWebView2Environment.CreateCoreWebView2ControllerWithOptionsAsync](corewebview2environment.md#createcorewebview2controllerwithoptionsasync) and [CoreWebView2Environment.CreateCoreWebView2CompositionControllerWithOptionsAsync](corewebview2environment.md#createcorewebview2compositioncontrollerwithoptionsasync) function for multiple profiles support.



### CreateCoreWebView2ControllerWithOptionsAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;[CoreWebView2Controller](corewebview2controller.md)&gt; CreateCoreWebView2ControllerWithOptionsAsync([CoreWebView2ControllerWindowReference](corewebview2controllerwindowreference.md) ParentWindow, [CoreWebView2ControllerOptions](corewebview2controlleroptions.md) options)

Create a new webview with [CoreWebView2ControllerOptions](corewebview2controlleroptions.md) as parameter for multiple profiles support.
If a new webview has been created, the IAsyncOperation will be immediately invoked.



### CreateCoreWebView2PointerInfo

> [CoreWebView2PointerInfo](corewebview2pointerinfo.md) CreateCoreWebView2PointerInfo()

Creates an empty [CoreWebView2PointerInfo](corewebview2pointerinfo.md).
The returned [CoreWebView2PointerInfo](corewebview2pointerinfo.md) needs to be populated with all of the relevant info before calling [CoreWebView2CompositionController.SendPointerInput](corewebview2compositioncontroller.md#sendpointerinput).



### CreatePrintSettings

> [CoreWebView2PrintSettings](corewebview2printsettings.md) CreatePrintSettings()

Creates the [CoreWebView2PrintSettings](corewebview2printsettings.md) used by the [CoreWebView2.PrintToPdfAsync](corewebview2.md#printtopdfasync) method.



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

> static string GetAvailableBrowserVersionString()

Gets the browser version info including channel name if it is not the stable channel or WebView2 Runtime.



### GetAvailableBrowserVersionString

> static string GetAvailableBrowserVersionString(string browserExecutableFolder)

Gets the browser version info including channel name if it is not the stable channel or WebView2 Runtime where `browserExecutableFolder` is the relative path to the folder that contains the WebView2 Runtime.



### GetProcessInfos

> [`IVectorView`](/uwp/api/Windows.Foundation.Collections.IVectorView-1)&lt;[CoreWebView2ProcessInfo](corewebview2processinfo.md)&gt; GetProcessInfos()

Returns the list of [CoreWebView2ProcessInfo](corewebview2processinfo.md).



### UpdateRuntimeAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;[CoreWebView2UpdateRuntimeResult](corewebview2updateruntimeresult.md)&gt; UpdateRuntimeAsync()

Try to update the installed Microsoft Edge WebView2 Runtime.
This will potentially result in a new version of the Edge WebView2 Runtime being installed and [CoreWebView2Environment.NewBrowserVersionAvailable](corewebview2environment.md#newbrowserversionavailable) event being raised.
There is no guarantee on the order of that event being raised and the completed handler being invoked.
Besides the [CoreWebView2Environment.NewBrowserVersionAvailable](corewebview2environment.md#newbrowserversionavailable) event, there will be no impact to any currently running WebView2s when the update is installed.

Even though the Edge WebView2 Runtime update is installed for the machine and available to all users, the update will happen silently and not show elevation prompt.
This will not impact Edge browser installations.

The latest version can always be queried using the [CoreWebView2Environment.GetAvailableBrowserVersionString](corewebview2environment.md#getavailablebrowserversionstring) API.

The [CoreWebView2Environment.UpdateRuntimeAsync](corewebview2environment.md#updateruntimeasync) method is only supported for an installed Edge WebView2 Runtime.
When running a fixed version Edge WebView2 Runtime or non stable channel Edge browser, this API will return `HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)`.

There could only be one active UpdateRuntime operation in an app process, calling this API before previous call is completed will fail with `HRESULT_FROM_WIN32(ERROR_BUSY)`.
Calling this API repeatedly in a short period of time, will also fail with `HRESULT_FROM_WIN32(ERROR_BUSY)`.
To protect accidental abuse of the update service, the implementation throttles the calls of this API to 3 times within 5 minutes in a process. The exact throttling limit can change in the future.

Edge update service can only support one update request at a time globally. If there is already an update operation running in the Edge update service, the result will be a [CoreWebView2UpdateRuntimeResult](corewebview2updateruntimeresult.md) with [CoreWebView2UpdateRuntimeStatus](corewebview2updateruntimestatus.md).UpdateAlreadyRunning.
As the running update could succeed or fail, the app should retry later if [CoreWebView2Environment.NewBrowserVersionAvailable](corewebview2environment.md#newbrowserversionavailable) event has not been raised.

The `UpdateRuntime` operation is associated with the CoreWebView2Environment object and any ongoing `UpdateRuntime` operation will be aborted when the associated CoreWebView2Environment along with the CoreWebView2 objects that are created by the CoreWebView2Environment object are all released.
In this case, the result will be a [CoreWebView2UpdateRuntimeResult](corewebview2updateruntimeresult.md) with [CoreWebView2UpdateRuntimeStatus](corewebview2updateruntimestatus.md).Failed [CoreWebView2UpdateRuntimeResult.Status](corewebview2updateruntimeresult.md#status) and `E_ABORT` [CoreWebView2UpdateRuntimeResult.ExtendedError](corewebview2updateruntimeresult.md#extendederror).




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
