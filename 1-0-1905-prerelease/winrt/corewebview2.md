---
description: WebView2 enables you to host web content using the latest Microsoft Edge browser and web technology.
title: CoreWebView2
ms.date: 06/12/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2
---

# CoreWebView2 Class



WebView2 enables you to host web content using the latest Microsoft Edge browser and web technology.

## Summary

Members|Description
--|--
[BrowserProcessId](#browserprocessid) | Gets the process ID of the browser process that hosts the WebView.
[CanGoBack](#cangoback) | `true` if the WebView is able to navigate to a previous page in the navigation history.
[CanGoForward](#cangoforward) | `true` if the WebView is able to navigate to a next page in the navigation history.
[ContainsFullScreenElement](#containsfullscreenelement) | Indicates if the WebView contains a fullscreen HTML element.
[CookieManager](#cookiemanager) | Gets the [CoreWebView2CookieManager](corewebview2cookiemanager.md) object associated with this CoreWebView2.
[CustomDataPartitionId](#customdatapartitionid) | Gets or sets the custom data partition id of the WebView.
[DefaultDownloadDialogCornerAlignment](#defaultdownloaddialogcorneralignment) | The default download dialog corner alignment.
[DefaultDownloadDialogMargin](#defaultdownloaddialogmargin) | The default download dialog margin relative to the WebView corner specified by [CoreWebView2.DefaultDownloadDialogCornerAlignment](corewebview2.md#defaultdownloaddialogcorneralignment).
[DocumentTitle](#documenttitle) | Gets the title for the current top-level document.
[Environment](#environment) | Exposes the [CoreWebView2Environment](corewebview2environment.md) used to create this CoreWebView2.
[FaviconUri](#faviconuri) | Get the Uri as a string of the current Favicon. This will be an empty string if the page does not have a Favicon.
[IsDefaultDownloadDialogOpen](#isdefaultdownloaddialogopen) | True if the default download dialog is currently open.
[IsDocumentPlayingAudio](#isdocumentplayingaudio) | Indicates whether any audio output from this CoreWebView2 is playing. `true` if audio is playing even if [CoreWebView2.IsMuted](corewebview2.md#ismuted) is true.
[IsMuted](#ismuted) | Indicates whether all audio output from this CoreWebView2 is muted or not. Set to true will mute this CoreWebView2, and set to false will unmute this CoreWebView2. `true` if audio is muted.
[IsSuspended](#issuspended) | Whether WebView is suspended.
[MemoryUsageTargetLevel](#memoryusagetargetlevel) | Desired [CoreWebView2MemoryUsageTargetLevel](corewebview2memoryusagetargetlevel.md) of a WebView.
[Profile](#profile) | The associated [CoreWebView2Profile](corewebview2profile.md) object of CoreWebView2.
[Settings](#settings) | Gets the [CoreWebView2Settings](corewebview2settings.md) object contains various modifiable settings for the running WebView.
[Source](#source) | Gets the URI of the current top level document.
[StatusBarText](#statusbartext) | The current text of the statusbar as defined by [Window.statusbar](https://developer.mozilla.org/docs/Web/API/Window/statusbar).
[AddHostObjectToScript](#addhostobjecttoscript) | Adds the provided host object to script running in the WebView with the specified name.
[AddScriptToExecuteOnDocumentCreatedAsync](#addscripttoexecuteondocumentcreatedasync) | Adds the provided JavaScript to a list of scripts that should be run after the global object has been created, but before the HTML document has been parsed and before any other script included by the HTML document is run.
[AddWebResourceRequestedFilter](#addwebresourcerequestedfilter) | This is an overload method that allows to subscribe to WebResourceRequested events received outside of main page
[AddWebResourceRequestedFilter](#addwebresourcerequestedfilter) | Adds a URI and resource context filter for the [CoreWebView2.WebResourceRequested](corewebview2.md#webresourcerequested) event.
[CallDevToolsProtocolMethodAsync](#calldevtoolsprotocolmethodasync) | Runs an asynchronous DevToolsProtocol method.
[CallDevToolsProtocolMethodForSessionAsync](#calldevtoolsprotocolmethodforsessionasync) | Runs an asynchronous `DevToolsProtocol` method for a specific session of an attached target.
[CapturePreviewAsync](#capturepreviewasync) | Captures an image of what WebView is displaying.
[ClearServerCertificateErrorActionsAsync](#clearservercertificateerroractionsasync) | Clears all cached decisions to proceed with TLS certificate errors from the [CoreWebView2.ServerCertificateErrorDetected](corewebview2.md#servercertificateerrordetected) event for all WebView2's sharing the same session.
[ClearVirtualHostNameToFolderMapping](#clearvirtualhostnametofoldermapping) | Clears a host name mapping for local folder that was added by [CoreWebView2.SetVirtualHostNameToFolderMapping](corewebview2.md#setvirtualhostnametofoldermapping).
[CloseDefaultDownloadDialog](#closedefaultdownloaddialog) | Close the default download dialog.
[ExecuteScriptAsync](#executescriptasync) | Runs JavaScript code from the `javaScript` parameter in the current top-level document rendered in the WebView.
[ExecuteScriptWithResultAsync](#executescriptwithresultasync) | Runs JavaScript code from the `javaScript` parameter in the current top-level document rendered in the WebView, The result of the execution is returned asynchronously in the [CoreWebView2ExecuteScriptResult](corewebview2executescriptresult.md) object which has methods and properties to obtain the successful result of script execution as well as any unhandled JavaScript exceptions.
[GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver) | Gets a DevTools Protocol event receiver that allows you to subscribe to a DevToolsProtocol event.
[GetFaviconAsync](#getfaviconasync) | Get the downloaded Favicon image for the current page and copy it to the image stream.
[GoBack](#goback) | Navigates the WebView to the previous page in the navigation history.
[GoForward](#goforward) | Navigates the WebView to the next page in the navigation history.
[Navigate](#navigate) | Causes a navigation of the top level document to the specified URI.
[NavigateToString](#navigatetostring) | Initiates a navigation to `htmlContent` as source HTML of a new document.
[NavigateWithWebResourceRequest](#navigatewithwebresourcerequest) | Navigates using a constructed [CoreWebView2WebResourceRequest](corewebview2webresourcerequest.md) object.
[OpenDefaultDownloadDialog](#opendefaultdownloaddialog) | Open the default download dialog.
[OpenDevToolsWindow](#opendevtoolswindow) | Opens the DevTools window for the current document in the WebView.
[OpenTaskManagerWindow](#opentaskmanagerwindow) | Opens the Browser Task Manager view as a new window in the foreground.
[PostSharedBufferToScript](#postsharedbuffertoscript) | Share a shared buffer object with script of the main frame in the WebView.
[PostWebMessageAsJson](#postwebmessageasjson) | Posts the specified `webMessageAsJson` to the top level document in this WebView.
[PostWebMessageAsString](#postwebmessageasstring) | Posts a message that is a simple string rather than a JSON string representation of a JavaScript object.
[PrintAsync](#printasync) | Print the current web page asynchronously to the specified printer with the provided settings.
[PrintToPdfAsync](#printtopdfasync) | Print the current page to PDF asynchronously with the provided settings.
[PrintToPdfStreamAsync](#printtopdfstreamasync) | Provides the Pdf data of current web page asynchronously for the provided settings.
[Reload](#reload) | Reloads the current page.
[RemoveHostObjectFromScript](#removehostobjectfromscript) | Removes the host object specified by the name so that it is no longer accessible from JavaScript code in the WebView.
[RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated) | Removes the corresponding JavaScript added via [CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync](corewebview2.md#addscripttoexecuteondocumentcreatedasync) with the specified script ID.
[RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter) | This is an overload method that allows to unsubscribe from WebResourceRequested events received outside of main page
[RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter) | Removes a matching WebResource filter that was previously added for the [CoreWebView2.WebResourceRequested](corewebview2.md#webresourcerequested) event.
[Resume](#resume) | Resumes the WebView so that it resumes activities on the web page.
[SetVirtualHostNameToFolderMapping](#setvirtualhostnametofoldermapping) | Sets a mapping between a virtual host name and a folder path to make available to web sites via that host name.
[ShowPrintUI](#showprintui) | Opens the print dialog to print the current web page.
[Stop](#stop) | Stops all navigations and pending resource fetches.
[TrySuspendAsync](#trysuspendasync) | An app may call this API to have the WebView2 consume less memory.
[BasicAuthenticationRequested](#basicauthenticationrequested) | BasicAuthenticationRequested event is raised when WebView encounters a Basic HTTP Authentication request as described in https://developer.mozilla.org/docs/Web/HTTP/Authentication, a Digest HTTP Authentication request as described in https://developer.mozilla.org/docs/Web/HTTP/Headers/Authorization#digest, an NTLM authentication or a Proxy Authentication request.
[ClientCertificateRequested](#clientcertificaterequested) | ClientCertificateRequested is raised when WebView2 is making a request to an HTTP server that needs a client certificate for HTTP authentication. Read more about HTTP client certificates at [RFC 8446 The Transport Layer Security (TLS) Protocol Version 1.3](https://tools.ietf.org/html/rfc8446).
[ContainsFullScreenElementChanged](#containsfullscreenelementchanged) | ContainsFullScreenElementChanged is raised when the [CoreWebView2.ContainsFullScreenElement](corewebview2.md#containsfullscreenelement) property changes.
[ContentLoading](#contentloading) | ContentLoading is raised before any content is loaded, including scripts added with [CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync](corewebview2.md#addscripttoexecuteondocumentcreatedasync). ContentLoading is not raised if a same page navigation occurs (such as through fragment navigations or `history.pushState` navigations).
[ContextMenuRequested](#contextmenurequested) | ContextMenuRequested is raised when a context menu is requested by the user and the content inside WebView hasn't disabled context menus.
[DOMContentLoaded](#domcontentloaded) | DOMContentLoaded is raised when the initial HTML document has been parsed.
[DocumentTitleChanged](#documenttitlechanged) | DocumentTitleChanged is raised when the [CoreWebView2.DocumentTitle](corewebview2.md#documenttitle) property changes and may be raised before or after the [CoreWebView2.NavigationCompleted](corewebview2.md#navigationcompleted) event.
[DownloadStarting](#downloadstarting) | DownloadStarting is raised when a download has begun, blocking the default download dialog, but not blocking the progress of the download.
[FaviconChanged](#faviconchanged) | Raised when the Favicon has changed. This can include when a new page is loaded and thus by default no icon is set or the icon is set for the page by DOM or JavaScript.
[FrameCreated](#framecreated) | FrameCreated is raised when a new iframe is created. Handle this event to get access to [CoreWebView2Frame](corewebview2frame.md) objects.
[FrameNavigationCompleted](#framenavigationcompleted) | FrameNavigationCompleted is raised when a child frame has completely loaded (`body.onload` has been raised) or loading stopped with error.
[FrameNavigationStarting](#framenavigationstarting) | FrameNavigationStarting is raised when a child frame in the WebView requests permission to navigate to a different URI.
[HistoryChanged](#historychanged) | HistoryChanged is raised for changes to joint session history, which consists of top-level and manual frame navigations.
[IsDefaultDownloadDialogOpenChanged](#isdefaultdownloaddialogopenchanged) | Raised when the [CoreWebView2.IsDefaultDownloadDialogOpen](corewebview2.md#isdefaultdownloaddialogopen) property changes.
[IsDocumentPlayingAudioChanged](#isdocumentplayingaudiochanged) | IsDocumentPlayingAudioChanged is raised when document starts or stops playing audio.
[IsMutedChanged](#ismutedchanged) | IsMutedChanged is raised when the mute state changes.
[LaunchingExternalUriScheme](#launchingexternalurischeme) | LaunchingExternalUriScheme is raised when a navigation request is made to a URI scheme that is registered with the OS.
[NavigationCompleted](#navigationcompleted) | NavigationCompleted is raised when the WebView has completely loaded (`body.onload` has been raised) or loading stopped with error.
[NavigationStarting](#navigationstarting) | NavigationStarting is raised when the WebView main frame is requesting permission to navigate to a different URI.
[NewWindowRequested](#newwindowrequested) | NewWindowRequested is raised when content inside the WebView requests to open a new window, such as through `window.open()`.
[PermissionRequested](#permissionrequested) | PermissionRequested is raised when content in a WebView requests permission to access some privileged resources.
[ProcessFailed](#processfailed) | ProcessFailed is raised when a WebView process ends unexpectedly or becomes unresponsive.
[ScriptDialogOpening](#scriptdialogopening) | ScriptDialogOpening is raised when a JavaScript dialog (`alert`, `confirm`, `prompt`, or `beforeunload`) displays for the WebView.
[ServerCertificateErrorDetected](#servercertificateerrordetected) | The ServerCertificateErrorDetected event is raised when the WebView2 cannot verify server's digital certificate while loading a web page.
[SourceChanged](#sourcechanged) | SourceChanged is raised when the [CoreWebView2.Source](corewebview2.md#source) property changes.
[StatusBarTextChanged](#statusbartextchanged) | StatusBarTextChanged event is raised when the text in the [Window.statusbar](https://developer.mozilla.org/docs/Web/API/Window/statusbar) changes. When the event is fired use the property [CoreWebView2.StatusBarText](corewebview2.md#statusbartext) to get the current statusbar text.
[WebMessageReceived](#webmessagereceived) | WebMessageReceived is raised when the [CoreWebView2Settings.IsWebMessageEnabled](corewebview2settings.md#iswebmessageenabled) setting is set and the top-level document of the WebView runs `window.chrome.webview.postMessage` or `window.chrome.webview.postMessageWithAdditionalObjects`.
[WebResourceRequested](#webresourcerequested) | WebResourceRequested is raised when the WebView is performing a URL request to a matching URL and resource context filter that was added with [CoreWebView2.AddWebResourceRequestedFilter](corewebview2.md#addwebresourcerequestedfilter).
[WebResourceResponseReceived](#webresourceresponsereceived) | WebResourceResponseReceived is raised when the WebView receives the response for a request for a web resource (any URI resolution performed by the WebView; such as HTTP/HTTPS, file and data requests from redirects, navigations, declarations in HTML, implicit Favicon lookups, and fetch API usage in the document).
[WindowCloseRequested](#windowcloserequested) | WindowCloseRequested is raised when content inside the WebView requested to close the window, such as after `window.close()` is run.

## Properties

### BrowserProcessId

> readonly  uint32_t BrowserProcessId

Gets the process ID of the browser process that hosts the WebView.

### CanGoBack

> readonly  bool CanGoBack

`true` if the WebView is able to navigate to a previous page in the navigation history.
If CanGoBack changes value, the [CoreWebView2.HistoryChanged](corewebview2.md#historychanged) event is raised.

### CanGoForward

> readonly  bool CanGoForward

`true` if the WebView is able to navigate to a next page in the navigation history.
If CanGoForward changes value, the [CoreWebView2.HistoryChanged](corewebview2.md#historychanged) event is raised.

### ContainsFullScreenElement

> readonly  bool ContainsFullScreenElement

Indicates if the WebView contains a fullscreen HTML element.

### CookieManager

> readonly  [CoreWebView2CookieManager](corewebview2cookiemanager.md) CookieManager

Gets the [CoreWebView2CookieManager](corewebview2cookiemanager.md) object associated with this CoreWebView2.

### CustomDataPartitionId

>  string CustomDataPartitionId

Gets or sets the custom data partition id of the WebView.
This API requires enabling 2 experimental browser features to work properly.
These features will be enabled by default in the future.
Before these features are enabled by default, please enable them by ensuring `--enable-features=ThirdPartyStoragePartitioning,PartitionedCookies` is set in [CoreWebView2EnvironmentOptions.AdditionalBrowserArguments](corewebview2environmentoptions.md#additionalbrowserarguments) used to initialize [CoreWebView2Environment](corewebview2environment.md).
If these features are not enabled, all data are treated as unpartitioned and stored in the global default location for the profile.
When custom data partition id id is set, the page in the WebView will act as if the page were hosted in a top level site uniquely associated with the partition id and have a separate storage partition as described in https://developer.chrome.com/docs/privacy-sandbox/storage-partitioning/ and separate cookie partition as described in https://developer.chrome.com/docs/privacy-sandbox/chips/ with all cookies partitioned.
If custom data partition id is set to null or empty string, the page inside the WebView will work normally with data treated as unpartitioned.
The custom data partition id is case sensitive. The default is an empty string. There is no restriction on the length or what characters can be used in partition id.
The change of the custom data partition id will be applied to new  page or iframe navigations and not impact existing pages and iframes.
To avoid accidentally using the new partition id for new page or iframe navigations started by the old page, it is recommended to create a new WebView for new partition instead of changing partition.
If you really have to change partition, it is recommended to navigate to a blank page before setting the new partition id and navigating to a page with the new partition.
As setting custom data partition id does not change DOM security model, developers should be very careful for WebViews with opener and opened window relationship, especially when the pages in the WebViews have same origin, like when the opened window is the same website or about:blank.
The pages in these WebViews can access each other????????s DOM and therefore can potentially access DOM storage and cookies in different partition for the same website.
It is recommended to set the same custom data partition id for these WebViews, unless there is an absolute need to set different partition ids and only trusted code is hosted in them.
:::code language="csharp" source="../code/sample/SampleApps/WebView2WpfBrowser/MainWindow.xaml.cs" id="CustomDataPartitionId":::

### DefaultDownloadDialogCornerAlignment

>  [CoreWebView2DefaultDownloadDialogCornerAlignment](corewebview2defaultdownloaddialogcorneralignment.md) DefaultDownloadDialogCornerAlignment

The default download dialog corner alignment.
The dialog can be aligned to any of the WebView corners (see [CoreWebView2DefaultDownloadDialogCornerAlignment](corewebview2defaultdownloaddialogcorneralignment.md)). When the WebView or dialog changes size, the dialog keeps it position relative to the corner. The dialog may become partially or completely outside of the WebView bounds if the WebView is small enough. Set the margin from the corner with the [CoreWebView2.DefaultDownloadDialogMargin](corewebview2.md#defaultdownloaddialogmargin) property. The corner alignment and margin should be set during initialization to ensure that they are correcly applied when the layout is first computed, otherwise they will not take effect until the next time the WebView position or size is updated.

### DefaultDownloadDialogMargin

>  [Point](/uwp/api/Windows.Foundation.Point) DefaultDownloadDialogMargin

The default download dialog margin relative to the WebView corner specified by [CoreWebView2.DefaultDownloadDialogCornerAlignment](corewebview2.md#defaultdownloaddialogcorneralignment).
The margin is a point that describes the vertical and horizontal distances between the chosen WebView corner and the default download dialog corner nearest to it. Positive values move the dialog towards the center of the WebView from the chosen WebView corner, and negative values move the dialog away from it. Use (0, 0) to align the dialog to the WebView corner with no margin. The corner alignment and margin should be set during initialization to ensure that they are correcly applied when the layout is first computed, otherwise they will not take effect until the next time the WebView position or size is updated.

### DocumentTitle

> readonly  string DocumentTitle

Gets the title for the current top-level document.
If the document has no explicit title or is otherwise empty, a default that may or may not match the URI of the document is used.

### Environment

> readonly  [CoreWebView2Environment](corewebview2environment.md) Environment

Exposes the [CoreWebView2Environment](corewebview2environment.md) used to create this CoreWebView2.

### FaviconUri

> readonly  string FaviconUri

Get the Uri as a string of the current Favicon. This will be an empty string if the page does not have a Favicon.

### IsDefaultDownloadDialogOpen

> readonly  bool IsDefaultDownloadDialogOpen

True if the default download dialog is currently open.
The value of this property changes only when the default download dialog is explicitly opened or closed. Hiding the WebView implicitly hides the dialog, but does not change the value of this property.

### IsDocumentPlayingAudio

> readonly  bool IsDocumentPlayingAudio

Indicates whether any audio output from this CoreWebView2 is playing. `true` if audio is playing even if [CoreWebView2.IsMuted](corewebview2.md#ismuted) is true.

### IsMuted

>  bool IsMuted

Indicates whether all audio output from this CoreWebView2 is muted or not. Set to true will mute this CoreWebView2, and set to false will unmute this CoreWebView2. `true` if audio is muted.

### IsSuspended

> readonly  bool IsSuspended

Whether WebView is suspended.
True when WebView is suspended, from the time when [CoreWebView2.TrySuspendAsync](corewebview2.md#trysuspendasync) has completed successfully until WebView is resumed.

### MemoryUsageTargetLevel

>  [CoreWebView2MemoryUsageTargetLevel](corewebview2memoryusagetargetlevel.md) MemoryUsageTargetLevel

Desired [CoreWebView2MemoryUsageTargetLevel](corewebview2memoryusagetargetlevel.md) of a WebView.
An app may set [CoreWebView2.MemoryUsageTargetLevel](corewebview2.md#memoryusagetargetlevel) to indicate desired memory consumption level of WebView.
Scripts will not be impacted and continue to run.
This is useful for inactive apps that still want to run scripts and/or keep network connections alive and therefore could not call [CoreWebView2.TrySuspendAsync](corewebview2.md#trysuspendasync) and [CoreWebView2.Resume](corewebview2.md#resume) to reduce memory consumption.
These apps can set memory usage target level to [CoreWebView2MemoryUsageTargetLevel](corewebview2memoryusagetargetlevel.md).Low when the app becomes inactive, and set back to [CoreWebView2MemoryUsageTargetLevel](corewebview2memoryusagetargetlevel.md).Normal when the app becomes active.

It is not necessary to set CoreWebView2Controller's IsVisible property to false when setting the property.

It is a best effort operation to change memory usage level, and the API will return before the operation completes.

Setting the level to [CoreWebView2MemoryUsageTargetLevel](corewebview2memoryusagetargetlevel.md).Low could potentially cause memory for some WebView browser processes to be swapped out to disk in some circumstances. It is a best effort to reduce memory usage as much as possible.
If a script runs after its related memory has been swapped out, the memory will be swapped back in to ensure the script can still run, but performance might be impacted.
Therefore, the app should set the level back to [CoreWebView2MemoryUsageTargetLevel](corewebview2memoryusagetargetlevel.md).Normal when the app becomes active again. Setting memory usage target level back to normal will not happen automatically.

An app should choose to use either the combination of [CoreWebView2.TrySuspendAsync](corewebview2.md#trysuspendasync) and [CoreWebView2.Resume](corewebview2.md#resume) or the combination of setting MemoryUsageTargetLevel to [CoreWebView2MemoryUsageTargetLevel](corewebview2memoryusagetargetlevel.md).Low and [CoreWebView2MemoryUsageTargetLevel](corewebview2memoryusagetargetlevel.md).Normal. It is not advisable to mix them.
Trying to set [CoreWebView2.MemoryUsageTargetLevel](corewebview2.md#memoryusagetargetlevel) while suspended will be ignored.
The [CoreWebView2.TrySuspendAsync](corewebview2.md#trysuspendasync) and [CoreWebView2.Resume](corewebview2.md#resume) methods will change the [CoreWebView2.MemoryUsageTargetLevel](corewebview2.md#memoryusagetargetlevel).
[CoreWebView2.TrySuspendAsync](corewebview2.md#trysuspendasync) will automatically set [CoreWebView2.MemoryUsageTargetLevel](corewebview2.md#memoryusagetargetlevel) to [CoreWebView2MemoryUsageTargetLevel](corewebview2memoryusagetargetlevel.md).Low while [CoreWebView2.Resume](corewebview2.md#resume) on suspended WebView will automatically set [CoreWebView2.MemoryUsageTargetLevel](corewebview2.md#memoryusagetargetlevel) to [CoreWebView2MemoryUsageTargetLevel](corewebview2memoryusagetargetlevel.md).Normal.
Calling [CoreWebView2.Resume](corewebview2.md#resume) when the WebView is not suspended would not change [CoreWebView2.MemoryUsageTargetLevel](corewebview2.md#memoryusagetargetlevel).

### Profile

> readonly  [CoreWebView2Profile](corewebview2profile.md) Profile

The associated [CoreWebView2Profile](corewebview2profile.md) object of CoreWebView2.

### Settings

> readonly  [CoreWebView2Settings](corewebview2settings.md) Settings

Gets the [CoreWebView2Settings](corewebview2settings.md) object contains various modifiable settings for the running WebView.

### Source

> readonly  string Source

Gets the URI of the current top level document.
This value potentially changes as a part of the [CoreWebView2.SourceChanged](corewebview2.md#sourcechanged) event raised for some cases such as navigating to a different site or fragment navigations. It remains the same for other types of navigations such as page refreshes or `history.pushState` with the same URL as the current page.

### StatusBarText

> readonly  string StatusBarText

The current text of the statusbar as defined by [Window.statusbar](https://developer.mozilla.org/docs/Web/API/Window/statusbar).



## Methods

### AddHostObjectToScript

> void AddHostObjectToScript(string name, Object rawObject)

Adds the provided host object to script running in the WebView with the specified name.
Host objects are exposed as host object proxies via `window.chrome.webview.hostObjects.{name}`. Host object proxies are promises and will resolve to an object representing the host object. Only the COM visible objects/properties/methods can be accessed from script.

JavaScript code in the WebView will be able to access appObject as following and then access attributes and methods of appObject.

Note that while simple types, `IDispatch` and array are supported, and `IUnknown` objects that also implement `IDispatch` are treated as `IDispatch`, generic `IUnknown`, `VT_DECIMAL`, or `VT_RECORD` variant is not supported. Remote JavaScript objects like callback functions are represented as an `VT_DISPATCH` VARIANT with the object implementing `IDispatch`. The JavaScript callback method may be invoked using DISPID_VALUE for the DISPID. Nested arrays are supported up to a depth of 3. Arrays of by reference types are not supported. `VT_EMPTY` and `VT_NULL` are mapped into JavaScript as `null`. In JavaScript `null` and `undefined` are mapped to `VT_EMPTY`.

Additionally, all host objects are exposed as `window.chrome.webview.hostObjects.sync.{name}`. Here the host objects are exposed as synchronous host object proxies. These are not promises and calls to functions or property access synchronously block running script waiting to communicate cross process for the host code to run. Accordingly this can result in reliability issues and it is recommended that you use the promise based asynchronous `window.chrome.webview.hostObjects.{name}` API described above.

Synchronous host object proxies and asynchronous host object proxies can both proxy the same host object. Remote changes made by one proxy will be reflected in any other proxy of that same host object whether the other proxies and synchronous or asynchronous.

While JavaScript is blocked on a synchronous call to native code, that native code is unable to call back to JavaScript. Attempts to do so will fail with `HRESULT_FROM_WIN32(ERROR_POSSIBLE_DEADLOCK)`.

Host object proxies are JavaScript Proxy objects that intercept all property get, property set, and method invocations. Properties or methods that are a part of the Function or Object prototype are run locally. Additionally any property or method in the array `chrome.webview.hostObjects.options.forceLocalProperties` will also be run locally. This defaults to including optional methods that have meaning in JavaScript like `toJSON` and `Symbol.toPrimitive`. You can add more to this array as required.

There's a method `chrome.webview.hostObjects.cleanupSome` that will best effort garbage collect host object proxies.

The `chrome.webview.hostObjects.options` object provides the ability to change some functionality of host objects.

Options property | Details
---|---
`forceLocalProperties` | This is an array of host object property names that will be run locally, instead of being called on the native host object. This defaults to `then`, `toJSON`, `Symbol.toString`, and `Symbol.toPrimitive`. You can add other properties to specify that they should be run locally on the JavaScript host object proxy.
`log` | This is a callback that will be called with debug information. For example, you can set this to `console.log.bind(console)` to have it print debug information to the console to help when troubleshooting host object usage. By default this is null.
`shouldSerializeDates` | By default this is false, and JavaScript Date objects will be sent to host objects as a string using `JSON.stringify`. You can set this property to true to have Date objects properly serialize as a `VT_DATE` when sending to the native host object, and have `VT_DATE` properties and return values create a JavaScript Date object.
`defaultSyncProxy` | When calling a method on a synchronous proxy, the result should also be a synchronous proxy. But in some cases, the sync/async context is lost (for example, when providing to native code a reference to a function, and then calling that function in native code). In these cases, the proxy will be asynchronous, unless this property is set.
`forceAsyncMethodMatches` | This is an array of regular expressions. When calling a method on a synchronous proxy, the method call will be performed asynchronously if the method name matches a string or regular expression in this array. Setting this value to `Async` will make any method that ends with Async be an asynchronous method call. If an async method doesn't match here and isn't forced to be asynchronous, the method will be invoked synchronously, blocking execution of the calling JavaScript and then returning the resolution of the promise, rather than returning a promise.
`ignoreMemberNotFoundError` | By default, an exception is thrown when attempting to get the value of a proxy property that doesn't exist on the corresponding native class. Setting this property to `true` switches the behavior to match Chakra WinRT projection (and general JavaScript) behavior of returning `undefined` with no error.

Host object proxies additionally have the following methods:

Method name | Details
---|---
`applyHostFunction`, `getHostProperty`, `setHostProperty` | Perform a method invocation, property get, or property set on the host object. Use the methods to explicitly force a method or property to run remotely if a conflicting local method or property exists.  For instance, `proxy.toString()` runs the local `toString` method on the proxy object. But proxy.applyHostFunction('toString') runs `toString` on the host proxied object instead.
`getLocalProperty`, `setLocalProperty` | Perform property get, or property set locally.  Use the methods to force getting or setting a property on the host object proxy rather than on the host object it represents. For instance, `proxy.unknownProperty` gets the property named `unknownProperty` from the host proxied object.  But proxy.getLocalProperty('unknownProperty') gets the value of the property `unknownProperty` on the proxy object.
`sync` | Asynchronous host object proxies expose a sync method which returns a promise for a synchronous host object proxy for the same host object.  For example, `chrome.webview.hostObjects.sample.methodCall()` returns an asynchronous host object proxy.  Use the `sync` method to obtain a synchronous host object proxy instead: `const syncProxy = await chrome.webview.hostObjects.sample.methodCall().sync()`.
`async` | Synchronous host object proxies expose an async method which blocks and returns an asynchronous host object proxy for the same host object.  For example, `chrome.webview.hostObjects.sync.sample.methodCall()` returns a synchronous host object proxy.  Running the `async` method on this blocks and then returns an asynchronous host object proxy for the same host object: `const asyncProxy = chrome.webview.hostObjects.sync.sample.methodCall().async()`.
`then` | Asynchronous host object proxies have a `then` method.  Allows proxies to be awaitable.  `then` returns a promise that resolves with a representation of the host object.  If the proxy represents a JavaScript literal, a copy of that is returned locally.  If the proxy represents a function, a non-awaitable proxy is returned.  If the proxy represents a JavaScript object with a mix of literal properties and function properties, the a copy of the object is returned with some properties as host object proxies.

All other property and method invocations (other than the above Remote object proxy methods, `forceLocalProperties` list, and properties on Function and Object prototypes) are run remotely. Asynchronous host object proxies return a promise representing asynchronous completion of remotely invoking the method, or getting the property. The promise resolves after the remote operations complete and the promises resolve to the resulting value of the operation. Synchronous host object proxies work similarly but block JavaScript execution and wait for the remote operation to complete.

Setting a property on an asynchronous host object proxy works slightly differently. The set returns immediately and the return value is the value that will be set. This is a requirement of the JavaScript Proxy object. If you need to asynchronously wait for the property set to complete, use the `setHostProperty` method which returns a promise as described above. Synchronous object property set property synchronously blocks until the property is set.

Exposing host objects to script has security risk. Please follow [best practices](/microsoft-edge/webview2/concepts/security).
To create a [IDispatch](/windows/win32/api/oaidl/nn-oaidl-idispatch) implementing class in C# use the following attributes on each class you intend to expose.
```csharp
// Bridge and BridgeAnotherClass are C# classes that implement IDispatch and works with AddHostObjectToScript.
[ClassInterface(ClassInterfaceType.AutoDual)]
[ComVisible(true)]
public class BridgeAnotherClass
{
    // Sample property.
    public string Prop { get; set; } = "Example";
}

[ClassInterface(ClassInterfaceType.AutoDual)]
[ComVisible(true)]
public class Bridge
{
    public string Func(string param)
    {
        return "Example: " + param;
    }

    public BridgeAnotherClass AnotherObject { get; set; } = new BridgeAnotherClass();

    // Sample indexed property.
    [System.Runtime.CompilerServices.IndexerName("Items")]
    public string this[int index]
    {
        get { return m_dictionary[index]; }
        set { m_dictionary[index] = value; }
    }
    private Dictionary&lt;int, string&gt; m_dictionary = new Dictionary&lt;int, string&gt;();
}
```
Then add instances of those classes via [CoreWebView2.AddHostObjectToScript](corewebview2.md#addhostobjecttoscript):
```csharp
webView.CoreWebView2.AddHostObjectToScript("bridge", new Bridge());
```
And then in script you can call the methods, and access those properties of the objects added via [CoreWebView2.AddHostObjectToScript](corewebview2.md#addhostobjecttoscript):
```csharp
// Find added objects on the hostObjects property
const bridge = chrome.webview.hostObjects.bridge;

// Call a method and pass in a parameter.
// The result is another proxy promise so you must await to get the result.
console.log(await bridge.Func("testing..."));

// A property may be another object as long as its class also implements
// IDispatch.
// Getting a property also gets a proxy promise you must await.
const propValue = await bridge.AnotherObject.Prop;
console.log(propValue);

// Indexed properties
let index = 123;
bridge[index] = "test";
let result = await bridge[index];
console.log(result);
```



### AddScriptToExecuteOnDocumentCreatedAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;string&gt; AddScriptToExecuteOnDocumentCreatedAsync(string javaScript)

Adds the provided JavaScript to a list of scripts that should be run after the global object has been created, but before the HTML document has been parsed and before any other script included by the HTML document is run.
The injected script will apply to all future top level document and child frame navigations until removed with [CoreWebView2.RemoveScriptToExecuteOnDocumentCreated](corewebview2.md#removescripttoexecuteondocumentcreated).
This is applied asynchronously and you must wait for the returned IAsyncOperation to complete before you can be sure that the script is ready to execute on future navigations.
If the method is run in [CoreWebView2.NewWindowRequested](corewebview2.md#newwindowrequested) handler, it should be called before the new window is set. For more details see [CoreWebView2NewWindowRequestedEventArgs.NewWindow](corewebview2newwindowrequestedeventargs.md#newwindow).

Note that if an HTML document has sandboxing of some kind via [sandbox](https://developer.mozilla.org/docs/Web/HTML/Element/iframe#attr-sandbox) properties or the [Content-Security-Policy HTTP header](https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Security-Policy) this will affect the script run here. So, for example, if the `allow-modals` keyword is not set then calls to the `alert` function will be ignored.



### AddWebResourceRequestedFilter

> void AddWebResourceRequestedFilter(string uri, [CoreWebView2WebResourceContext](corewebview2webresourcecontext.md) resourceContext, [CoreWebView2WebResourceRequestSourceKinds](corewebview2webresourcerequestsourcekinds.md) requestSourceKinds)

This is an overload method that allows to subscribe to WebResourceRequested events received outside of main page



### AddWebResourceRequestedFilter

> void AddWebResourceRequestedFilter(string uri, [CoreWebView2WebResourceContext](corewebview2webresourcecontext.md) ResourceContext)

Adds a URI and resource context filter for the [CoreWebView2.WebResourceRequested](corewebview2.md#webresourcerequested) event.
A web resource request with a resource context that matches this filter's resource context and a URI that matches this filter's URI wildcard string will be raised via the [CoreWebView2.WebResourceRequested](corewebview2.md#webresourcerequested) event.

The `uri` parameter value is a wildcard string matched against the URI of the web resource request. This is a glob style wildcard string in which a `*` matches zero or more characters and a `?` matches exactly one character.
These wildcard characters can be escaped using a backslash just before the wildcard character in order to represent the literal `*` or `?`.

The matching occurs over the URI as a whole string and not limiting wildcard matches to particular parts of the URI.
The wildcard filter is compared to the URI after the URI has been normalized, any URI fragment has been removed, and non-ASCII hostnames have been converted to punycode.

Specifying a `nullptr` for the uri is equivalent to an empty string which matches no URIs.

For more information about resource context filters, navigate to [CoreWebView2WebResourceContext](corewebview2webresourcecontext.md).

| URI Filter String | Request URI | Match | Notes |
| ---- | ---- | ---- | ---- |
| `*` | `https://contoso.com/a/b/c` | Yes | A single * will match all URIs |
| `*://contoso.com/*` | `https://contoso.com/a/b/c` | Yes | Matches everything in contoso.com across all schemes |
| `*://contoso.com/*` | `https://example.com/?https://contoso.com/` | Yes | But also matches a URI with just the same text anywhere in the URI |
| `example` | `https://contoso.com/example` | No | The filter does not perform partial matches |
| `*example` | `https://contoso.com/example` | Yes | The filter matches across URI parts |
| `*example` | `https://contoso.com/path/?example` | Yes | The filter matches across URI parts |
| `*example` | `https://contoso.com/path/?query#example` | No | The filter is matched against the URI with no fragment |
| `*example` | `https://example` | No | The URI is normalized before filter matching so the actual URI used for comparison is `https://example.com/` |
| `*example/` | `https://example` | Yes | Just like above, but this time the filter ends with a / just like the normalized URI |
| `https://xn--qei.example/` | `https://&#x2764;.example/` | Yes | Non-ASCII hostnames are normalized to punycode before wildcard comparison |
| `https://&#x2764;.example/` | `https://xn--qei.example/` | No | Non-ASCII hostnames are normalized to punycode before wildcard comparison |



### CallDevToolsProtocolMethodAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;string&gt; CallDevToolsProtocolMethodAsync(string methodName, string parametersAsJson)

Runs an asynchronous DevToolsProtocol method.
For more information about available methods, navigate to [DevTools Protocol Viewer](https://aka.ms/DevToolsProtocolDocs). The returned task is completed when the method asynchronously completes and will return the method's return object as a JSON string. Note even though WebView2 dispatches the CDP messages in the order called, CDP method calls may be processed out of order. If you require CDP methods to run in a particular order, you should await for the previous method call.



### CallDevToolsProtocolMethodForSessionAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;string&gt; CallDevToolsProtocolMethodForSessionAsync(string sessionId, string methodName, string parametersAsJson)

Runs an asynchronous `DevToolsProtocol` method for a specific session of an attached target.
There could be multiple `DevToolsProtocol` targets in a WebView.
Besides the top level page, iframes from different origin and web workers are also separate targets.
Attaching to these targets allows interaction with them.
When the DevToolsProtocol is attached to a target, the connection is identified by a sessionId.

To use this API, you must set the `flatten` parameter to true when calling `Target.attachToTarget` or `Target.setAutoAttach` `DevToolsProtocol` method.
Using `Target.setAutoAttach` is recommended as that would allow you to attach to dedicated worker targets, which are not discoverable via other APIs like `Target.getTargets`.
For more information about targets and sessions, navigate to [Chrome DevTools Protocol - Target domain]( https://chromedevtools.github.io/devtools-protocol/tot/Target).

For more information about available methods, navigate to [DevTools Protocol Viewer](https://aka.ms/DevToolsProtocolDocs). The handler's Invoke method will be called when the method asynchronously completes. Invoke will be called with the method's return object as a JSON string.



### CapturePreviewAsync

> [IAsyncAction](/uwp/api/Windows.Foundation.IAsyncAction) CapturePreviewAsync([CoreWebView2CapturePreviewImageFormat](corewebview2capturepreviewimageformat.md) imageFormat, [IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) imageStream)

Captures an image of what WebView is displaying.
When CapturePreviewAsync finishes writing to the stream, the Invoke method on the provided handler parameter is called. This method fails if called before the first [CoreWebView2.ContentLoading](corewebview2.md#contentloading) event. For example if this is called in the [CoreWebView2.NavigationStarting](corewebview2.md#navigationstarting) event for the first navigation it will fail. For subsequent navigations, the method may not fail, but will not capture an image of a given webpage until the [CoreWebView2.ContentLoading](corewebview2.md#contentloading) event has been fired for it. Any call to this method prior to that will result in a capture of the page being navigated away from.



### ClearServerCertificateErrorActionsAsync

> [IAsyncAction](/uwp/api/Windows.Foundation.IAsyncAction) ClearServerCertificateErrorActionsAsync()

Clears all cached decisions to proceed with TLS certificate errors from the [CoreWebView2.ServerCertificateErrorDetected](corewebview2.md#servercertificateerrordetected) event for all WebView2's sharing the same session.



### ClearVirtualHostNameToFolderMapping

> void ClearVirtualHostNameToFolderMapping(string hostName)

Clears a host name mapping for local folder that was added by [CoreWebView2.SetVirtualHostNameToFolderMapping](corewebview2.md#setvirtualhostnametofoldermapping).



### CloseDefaultDownloadDialog

> void CloseDefaultDownloadDialog()

Close the default download dialog.
Calling this method raises the [CoreWebView2.IsDefaultDownloadDialogOpenChanged](corewebview2.md#isdefaultdownloaddialogopenchanged) event if the dialog was open. No effect if the dialog is already closed.



### ExecuteScriptAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;string&gt; ExecuteScriptAsync(string javaScript)

Runs JavaScript code from the `javaScript` parameter in the current top-level document rendered in the WebView.
If the result is `undefined`, contains a reference cycle, or otherwise is not able to be encoded into JSON, the JSON `null` value is returned as the `"null"` string.

A function that has no explicit return value returns `undefined`. If the script that was run throws an unhandled exception, then the result is also `null`. This method is applied asynchronously. If the method is run after the [CoreWebView2.NavigationStarting](corewebview2.md#navigationstarting) event during a navigation, the script runs in the new document when loading it, around the time [CoreWebView2.ContentLoading](corewebview2.md#contentloading) is run. This operation works even if [CoreWebView2Settings.IsScriptEnabled](corewebview2settings.md#isscriptenabled) is set to `false`.



### ExecuteScriptWithResultAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;[CoreWebView2ExecuteScriptResult](corewebview2executescriptresult.md)&gt; ExecuteScriptWithResultAsync(string javaScript)

Runs JavaScript code from the `javaScript` parameter in the current top-level document rendered in the WebView, The result of the execution is returned asynchronously in the [CoreWebView2ExecuteScriptResult](corewebview2executescriptresult.md) object which has methods and properties to obtain the successful result of script execution as well as any unhandled JavaScript exceptions.



### GetDevToolsProtocolEventReceiver

> [CoreWebView2DevToolsProtocolEventReceiver](corewebview2devtoolsprotocoleventreceiver.md) GetDevToolsProtocolEventReceiver(string eventName)

Gets a DevTools Protocol event receiver that allows you to subscribe to a DevToolsProtocol event.
For more information about DevToolsProtocol events description and event args, navigate to [DevTools Protocol Viewer](https://aka.ms/DevToolsProtocolDocs).



### GetFaviconAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;[IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream)&gt; GetFaviconAsync([CoreWebView2FaviconImageFormat](corewebview2faviconimageformat.md) format)

Get the downloaded Favicon image for the current page and copy it to the image stream.
An `IStream` populated with the downloaded Favicon.



### GoBack

> void GoBack()

Navigates the WebView to the previous page in the navigation history.



### GoForward

> void GoForward()

Navigates the WebView to the next page in the navigation history.



### Navigate

> void Navigate(string uri)

Causes a navigation of the top level document to the specified URI.
For more information, navigate to [Navigation event](/microsoft-edge/webview2/concepts/navigation-events). Note that this operation starts a navigation and the corresponding [CoreWebView2.NavigationStarting](corewebview2.md#navigationstarting) event is raised sometime after Navigate runs.



### NavigateToString

> void NavigateToString(string htmlContent)

Initiates a navigation to `htmlContent` as source HTML of a new document.
The `htmlContent` parameter may not be larger than 2 MB (2 * 1024 * 1024 bytes) in total size. The origin of the new page is `about:blank`.
```csharp
webView.CoreWebView2.SetVirtualHostNameToFolderMapping(
    "appassets.example", "assets", CoreWebView2HostResourceAccessKind.DenyCors);
string htmlContent =
@"
    <head><link rel='stylesheet' href ='http://appassets.example/run.css' /></head>
    <body>
        <img src='http://appassets.example/grill.png' />
        <p><a href='http://appassets.example/winrt_test.txt'> Click me</a></p>
    </body>
";
webview.NavigateToString(htmlContent);
```



### NavigateWithWebResourceRequest

> void NavigateWithWebResourceRequest([CoreWebView2WebResourceRequest](corewebview2webresourcerequest.md) Request)

Navigates using a constructed [CoreWebView2WebResourceRequest](corewebview2webresourcerequest.md) object.
The headers in the [CoreWebView2WebResourceRequest](corewebview2webresourcerequest.md) override headers added by WebView2 runtime except for Cookie headers. Method can only be either `GET` or `POST`. Provided post data will only be sent only if the method is `POST` and the uri scheme is `HTTP(S)`.



### OpenDefaultDownloadDialog

> void OpenDefaultDownloadDialog()

Open the default download dialog.
If the dialog is opened before there are recent downloads, the dialog shows all past downloads for the current profile. Otherwise, the dialog shows only the recent downloads with a "See more" button for past downloads. Calling this method raises the [CoreWebView2.IsDefaultDownloadDialogOpenChanged](corewebview2.md#isdefaultdownloaddialogopenchanged) event if the dialog was closed. No effect if the dialog is already open.



### OpenDevToolsWindow

> void OpenDevToolsWindow()

Opens the DevTools window for the current document in the WebView.
Does nothing if run when the DevTools window is already open.



### OpenTaskManagerWindow

> void OpenTaskManagerWindow()

Opens the Browser Task Manager view as a new window in the foreground.
If the Browser Task Manager is already open, this will bring it into the foreground. WebView2 currently blocks the Shift+Esc shortcut for opening the task manager. An end user can open the browser task manager manually via the `Browser task manager` entry of the DevTools window's title bar's context menu.



### PostSharedBufferToScript

> void PostSharedBufferToScript([CoreWebView2SharedBuffer](corewebview2sharedbuffer.md) sharedBuffer, [CoreWebView2SharedBufferAccess](corewebview2sharedbufferaccess.md) access, string additionalDataAsJson)

Share a shared buffer object with script of the main frame in the WebView.
The script will receive a `sharedbufferreceived` event from chrome.webview.
The event arg for that event will have the following methods and properties.

| Property | Description |
|---|---|
| getBuffer() | A method that returns an ArrayBuffer object with the backing content from the shared buffer. |
| additionalData | An object as the result of parsing `additionalDataAsJson` as JSON string. This property will be `undefined` if `additionalDataAsJson` is nullptr or empty string. |
| source | With a value set as `chrome.webview` object. |

If `access` is [CoreWebView2SharedBufferAccess](corewebview2sharedbufferaccess.md).ReadOnly, the script will only have read access to the buffer.
If the script tries to modify the content in a read only buffer, it will cause an access violation in WebView renderer process and crash the renderer process.

If the shared buffer is already closed, the API throws COMException with error code of `RO_E_CLOSED`.
The script code should call `chrome.webview.releaseBuffer` with the shared buffer as the parameter to release underlying resources as soon as it does not need access to the shared buffer any more.

The application can post the same shared buffer object to multiple web pages or iframes, or post to the same web page or iframe multiple times.
Each `PostSharedBufferToScript` will create a separate ArrayBuffer object with its own view of the memory and is separately released.
The underlying shared memory will be released when all the views are released.

Sharing a buffer to script has security risk. You should only share buffer with trusted site.
If a buffer is shared to a untrusted site, possible sensitive information could be leaked.
If a buffer is shared as modifiable by the script and the script modifies it in an unexpected way, it could result in corrupted data that might even crash the application.

The example code shows how to send data to script for one time read only consumption.
:::code language="csharp" source="../code/sample/SampleApps/WebView2WpfBrowser/MainWindow.xaml.cs" id="OneTimeShareBuffer":::
:::code language="csharp" source="../code/sample/SampleApps/WebView2WpfBrowser/assets/sharedBuffer.html" id="ShareBufferScriptCode_1":::
:::code language="csharp" source="../code/sample/SampleApps/WebView2WpfBrowser/assets/sharedBuffer.html" id="ShareBufferScriptCode_2":::



### PostWebMessageAsJson

> void PostWebMessageAsJson(string webMessageAsJson)

Posts the specified `webMessageAsJson` to the top level document in this WebView.
The event args is an instance of `MessageEvent`. The [CoreWebView2Settings.IsWebMessageEnabled](corewebview2settings.md#iswebmessageenabled) setting must be `true` or the message will not be sent. The event arg's `data` property of the event arg is the `webMessageAsJson` string parameter parsed as a JSON string into a JavaScript object. The event arg's `source` property of the event arg is a reference to the `window.chrome.webview` object. For information about sending messages from the HTML document in the WebView to the host, navigate to [CoreWebView2.WebMessageReceived](corewebview2.md#webmessagereceived). The message is sent asynchronously. If a navigation occurs before the message is posted to the page, the message is not be sent.
Runs the message event of the `window.chrome.webview` of the top-level document. JavaScript in that document may subscribe and unsubscribe to the event using the following code:
```javascript
window.chrome.webview.addEventListener('message', handler)
window.chrome.webview.removeEventListener('message', handler)
```



### PostWebMessageAsString

> void PostWebMessageAsString(string webMessageAsString)

Posts a message that is a simple string rather than a JSON string representation of a JavaScript object.
This behaves in exactly the same manner as [CoreWebView2.PostWebMessageAsJson](corewebview2.md#postwebmessageasjson), but the `data` property of the event arg of the `window.chrome.webview` message is a string with the same value as `webMessageAsString`. Use this instead of [CoreWebView2.PostWebMessageAsJson](corewebview2.md#postwebmessageasjson) if you want to communicate using simple strings rather than JSON objects.



### PrintAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;[CoreWebView2PrintStatus](corewebview2printstatus.md)&gt; PrintAsync([CoreWebView2PrintSettings](corewebview2printsettings.md) printSettings)

Print the current web page asynchronously to the specified printer with the provided settings.
See [CoreWebView2PrintSettings](corewebview2printsettings.md) for description of settings. Passing null for `printSettings` results in default print settings used.

The method will return [CoreWebView2PrintStatus](corewebview2printstatus.md) as [CoreWebView2PrintStatus](corewebview2printstatus.md).PrinterUnavailable if `printerName` doesn't match with the name of any installed printers on the user OS.
The method will throw ArgumentException if the caller provides invalid settings for a given printer.

The async Print operation completes when it finishes printing to the printer. Only one `Printing` operation can be in progress at a time. If `Print` is called while a [CoreWebView2.PrintAsync](corewebview2.md#printasync) or [CoreWebView2.PrintToPdfAsync](corewebview2.md#printtopdfasync) or [CoreWebView2.PrintToPdfStreamAsync](corewebview2.md#printtopdfstreamasync) job is in progress, the IAsyncOperation throws exception. This is only for printing operation on one webview.

|       Error         |      PrintStatus                              |               Notes                                                                           |
| --- | --- | ---     |
|        No           | CoreWebView2PrintStatus.Succeeded             | Print operation succeeded.                                                                    |
|        No           | CoreWebView2PrintStatus.PrinterUnavailable    | If specified printer is not found or printer status is not available, offline or error state. |
|        No           | CoreWebView2PrintStatus.OtherError            | Print operation is failed.                                                                    |
|   ArgumentException | CoreWebView2PrintStatus.OtherError            | If the caller provides invalid settings for the specified printer.                            |
|      Exception      | CoreWebView2PrintStatus.OtherError            | Print operation is failed as printing job already in progress.                                |



### PrintToPdfAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;bool&gt; PrintToPdfAsync(string ResultFilePath, [CoreWebView2PrintSettings](corewebview2printsettings.md) printSettings)

Print the current page to PDF asynchronously with the provided settings.
See [CoreWebView2PrintSettings](corewebview2printsettings.md) for description of settings. Passing null for `printSettings` results in default print settings used.

Use `resultFilePath` to specify the path to the PDF file. The host should provide an absolute path, including file name. If the path points to an existing file, the file will be overwritten. If the path is not valid, the method fails.

The async PrintToPdf operation completes when the data has been written to the PDF file. If the application exits before printing is complete, the file is not saved. Only one PrintToPdf operation can be in progress at a time.
If PrintToPdf is called while a print to PDF operation is in progress, the IAsyncOperation completes and returns false.



### PrintToPdfStreamAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;[IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream)&gt; PrintToPdfStreamAsync([CoreWebView2PrintSettings](corewebview2printsettings.md) printSettings)

Provides the Pdf data of current web page asynchronously for the provided settings.
Stream will be rewound to the start of the pdf data.

See [CoreWebView2PrintSettings](corewebview2printsettings.md) for description of settings. Passing null for `printSettings` results in default print settings used.

The async PrintToPdfStream operation completes when it finishes writing to the stream. Only one `Printing` operation can be in progress at a time. If [CoreWebView2.PrintToPdfStreamAsync](corewebview2.md#printtopdfstreamasync) is called while a [CoreWebView2.PrintToPdfStreamAsync](corewebview2.md#printtopdfstreamasync) or [CoreWebView2.PrintToPdfAsync](corewebview2.md#printtopdfasync) or [CoreWebView2.PrintAsync](corewebview2.md#printasync) job is in progress, the IAsyncOperation throws an exception. This is only for printing operation on one webview.



### Reload

> void Reload()

Reloads the current page.
This is similar to navigating to the URI of current top level document including all navigation events firing and respecting any entries in the HTTP cache. But, the back or forward history will not be modified.



### RemoveHostObjectFromScript

> void RemoveHostObjectFromScript(string name)

Removes the host object specified by the name so that it is no longer accessible from JavaScript code in the WebView.
While new access attempts are denied, if the object is already obtained by JavaScript code in the WebView, the JavaScript code continues to have access to that object. Running this method for a name that is already removed or never added fails.



### RemoveScriptToExecuteOnDocumentCreated

> void RemoveScriptToExecuteOnDocumentCreated(string id)

Removes the corresponding JavaScript added via [CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync](corewebview2.md#addscripttoexecuteondocumentcreatedasync) with the specified script ID.
Both use [CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync](corewebview2.md#addscripttoexecuteondocumentcreatedasync) and this method in [CoreWebView2.NewWindowRequested](corewebview2.md#newwindowrequested) handler at the same time sometimes causes trouble. Since invalid scripts will be ignored, the script IDs you got may not be valid anymore.



### RemoveWebResourceRequestedFilter

> void RemoveWebResourceRequestedFilter(string uri, [CoreWebView2WebResourceContext](corewebview2webresourcecontext.md) resourceContext, [CoreWebView2WebResourceRequestSourceKinds](corewebview2webresourcerequestsourcekinds.md) requestSourceKinds)

This is an overload method that allows to unsubscribe from WebResourceRequested events received outside of main page



### RemoveWebResourceRequestedFilter

> void RemoveWebResourceRequestedFilter(string uri, [CoreWebView2WebResourceContext](corewebview2webresourcecontext.md) ResourceContext)

Removes a matching WebResource filter that was previously added for the [CoreWebView2.WebResourceRequested](corewebview2.md#webresourcerequested) event.
If the same filter was added multiple times, then it must need to be removed as many times as it was added for the removal to be effective.



### Resume

> void Resume()

Resumes the WebView so that it resumes activities on the web page.
This API can be called while the WebView2 controller is invisible.

The app can interact with the WebView immediately after [CoreWebView2.Resume](corewebview2.md#resume).

WebView will be automatically resumed when it becomes visible.



### SetVirtualHostNameToFolderMapping

> void SetVirtualHostNameToFolderMapping(string hostName, string folderPath, [CoreWebView2HostResourceAccessKind](corewebview2hostresourceaccesskind.md) accessKind)

Sets a mapping between a virtual host name and a folder path to make available to web sites via that host name.
After setting the mapping, documents loaded in the WebView can use HTTP or HTTPS URLs at the specified host name specified by `hostName` to access files in the local folder specified by `folderPath`.
This mapping applies to both top-level document and iframe navigations as well as subresource references from a document. This also applies to dedicated and shared worker scripts but does not apply to service worker scripts.

Due to a current implementation limitation, media files accessed using virtual host name can be very slow to load.

As the resource loaders for the current page might have already been created and running, changes to the mapping might not be applied to the current page and a reload of the page is needed to apply the new mapping.

Both absolute and relative paths are supported for `folderPath`. Relative paths are interpreted as relative to the folder where the exe of the app is in.
For example, after calling `SetVirtualHostNameToFolderMapping("appassets.example", "assets", CoreWebView2HostResourceAccessKind.Deny);`, navigating to `https://appassets.example/my-local-file.html` will show content from my-local-file.html in the assets subfolder located on disk under the same path as the app's executable file.

DOM elements that want to reference local files will have their host reference virtual host in the source. If there are multiple folders being used, define one unique virtual host per folder.
You should typically choose virtual host names that are never used by real sites.
If you own a domain such as `example.com`, another option is to use a subdomain reserved for the app (like `my-app.example.com`).
[RFC 6761](https://tools.ietf.org/html/rfc6761) has reserved several special-use domain names that are guaranteed to not be used by real sites (for example, `.example`, `.test`, and `.invalid`).
Note that using `.local` as the top-level domain name will work but can cause a delay during navigations. You should avoid using `.local` if you can.
Apps should use distinct domain names when mapping folder from different sources that should be isolated from each other. For instance, the app might use app-file.example for files that ship as part of the app, and book1.example might be used for files containing books from a less trusted source that were previously downloaded and saved to the disk by the app.
The host name used in the APIs is canonicalized using Chromium's host name parsing logic before being used internally.
For more information see [HTML5 2.6 URLs](https://dev.w3.org/html5/spec-LC/urls.html).
All host names that are canonicalized to the same string are considered identical.
For example, `EXAMPLE.COM` and `example.com` are treated as the same host name.
An international host name and its Punycode-encoded host name are considered the same host name. There is no DNS resolution for host name and the trailing '.' is not normalized as part of canonicalization.
Therefore `example.com` and `example.com.` are treated as different host names. Similarly, `virtual-host-name` and `virtual-host-name.example.com` are treated as different host names even if the machine has a DNS suffix of `example.com`.
Specify the minimal cross-origin access necessary to run the app. If there is not a need to access local resources from other origins, use [CoreWebView2HostResourceAccessKind](corewebview2hostresourceaccesskind.md).Deny.
Setting the `accessKind` parameter does not adjust the app container permission for a folder.
```csharp
webView.CoreWebView2.SetVirtualHostNameToFolderMapping(
    "appassets.example", "assets", CoreWebView2HostResourceAccessKind.DenyCors);
webView.Source = new Uri("https://appassets.example/index.html");
```

This in an example on how to embed a local image. For more information see [CoreWebView2.NavigateToString](corewebview2.md#navigatetostring).
```csharp
webView.CoreWebView2.SetVirtualHostNameToFolderMapping(
    "appassets.example", "assets", CoreWebView2HostResourceAccessKind.DenyCors);
string c_navString = "<img src='http://appassets.example/wv2.png'/>";
webview.NavigateToString(c_navString);
```



### ShowPrintUI

> void ShowPrintUI([CoreWebView2PrintDialogKind](corewebview2printdialogkind.md) printDialogKind)

Opens the print dialog to print the current web page.
See [CoreWebView2PrintDialogKind](corewebview2printdialogkind.md) for descriptions of print dialog kinds.

Invoking browser or system print dialog doesn't open new print dialog if it is already open.



### Stop

> void Stop()

Stops all navigations and pending resource fetches.
Does not stop scripts.



### TrySuspendAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;bool&gt; TrySuspendAsync()

An app may call this API to have the WebView2 consume less memory.
This is useful when a Win32 app becomes invisible, or when a Universal Windows Platform app is being suspended, during the suspended event handler before completing the suspended event.

The [CoreWebView2Controller.IsVisible](corewebview2controller.md#isvisible) property must be false when the API is called. Otherwise, the API throws COMException with error code of `HRESULT_FROM_WIN32(ERROR_INVALID_STATE)`.

Suspending is similar to putting a tab to sleep in the Edge browser. Suspending pauses WebView script timers and animations, minimizes CPU usage for the associated browser renderer process and allows the operating system to reuse the memory that was used by the renderer process for other processes.

Note that Suspend is best effort and considered completed successfully once the request is sent to browser renderer process. If there is a running script, the script will continue to run and the renderer process will be suspended after that script is done.

See [Sleeping Tabs FAQ](https://techcommunity.microsoft.com/t5/articles/sleeping-tabs-faq/m-p/1705434) for conditions that might prevent WebView from being suspended. In those situations, the result of the async task is false.

The WebView will be automatically resumed when it becomes visible. Therefore, the app normally does not have to call [CoreWebView2.Resume](corewebview2.md#resume) explicitly.

The app can call [CoreWebView2.Resume](corewebview2.md#resume) and then [CoreWebView2.TrySuspendAsync](corewebview2.md#trysuspendasync) periodically for an invisible WebView so that the invisible WebView can sync up with latest data and the page ready to show fresh content when it becomes visible.

All WebView APIs can still be accessed when a WebView is suspended. Some APIs like Navigate will auto resume the WebView. To avoid unexpected auto resume, check [CoreWebView2.IsSuspended](corewebview2.md#issuspended) property before calling APIs that might change WebView state.




## Events

### BasicAuthenticationRequested

BasicAuthenticationRequested event is raised when WebView encounters a Basic HTTP Authentication request as described in https://developer.mozilla.org/docs/Web/HTTP/Authentication, a Digest HTTP Authentication request as described in https://developer.mozilla.org/docs/Web/HTTP/Headers/Authorization#digest, an NTLM authentication or a Proxy Authentication request.
The host can provide a response with credentials for the authentication or cancel the request. If the host sets the Cancel property to false but does not provide either UserName or Password properties on the Response property, then WebView2 will show the default authentication challenge dialog prompt to the user.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2, [CoreWebView2BasicAuthenticationRequestedEventArgs](corewebview2basicauthenticationrequestedeventargs.md)&gt;

### ClientCertificateRequested

ClientCertificateRequested is raised when WebView2 is making a request to an HTTP server that needs a client certificate for HTTP authentication. Read more about HTTP client certificates at [RFC 8446 The Transport Layer Security (TLS) Protocol Version 1.3](https://tools.ietf.org/html/rfc8446).
The host have several options for responding to client certificate requests:

Scenario                                                   | Handled | Cancel | SelectedCertificate
---------------------------------------------------------- | ------- | ------ | -------------------
Respond to server with a certificate                       | True    | False  | MutuallyTrustedCertificate value
Respond to server without certificate                      | True    | False  | null
Display default client certificate selection dialog prompt | False   | False  | n/a
Cancel the request                                         | n/a     | True   | n/a

If the host don't handle the event, WebView2 will show the default client certificate selection dialog prompt to the user.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2, [CoreWebView2ClientCertificateRequestedEventArgs](corewebview2clientcertificaterequestedeventargs.md)&gt;

### ContainsFullScreenElementChanged

ContainsFullScreenElementChanged is raised when the [CoreWebView2.ContainsFullScreenElement](corewebview2.md#containsfullscreenelement) property changes.
An HTML element inside the WebView may enter fullscreen to the size of the WebView or leave fullscreen. This event is useful when, for example, a video element requests to go fullscreen. The listener of this event may resize the WebView in response.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2, Object&gt;

### ContentLoading

ContentLoading is raised before any content is loaded, including scripts added with [CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync](corewebview2.md#addscripttoexecuteondocumentcreatedasync). ContentLoading is not raised if a same page navigation occurs (such as through fragment navigations or `history.pushState` navigations).
This operation follows the [CoreWebView2.NavigationStarting](corewebview2.md#navigationstarting) and [CoreWebView2.SourceChanged](corewebview2.md#sourcechanged) events and precedes the [CoreWebView2.HistoryChanged](corewebview2.md#historychanged) and [CoreWebView2.NavigationCompleted](corewebview2.md#navigationcompleted) events.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2, [CoreWebView2ContentLoadingEventArgs](corewebview2contentloadingeventargs.md)&gt;

### ContextMenuRequested

ContextMenuRequested is raised when a context menu is requested by the user and the content inside WebView hasn't disabled context menus.
The host has the option to create their own context menu with the information provided in the event or can add items to or remove items from WebView context menu. If the host doesn't handle the event, WebView will display the default context menu.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2, [CoreWebView2ContextMenuRequestedEventArgs](corewebview2contextmenurequestedeventargs.md)&gt;

### DOMContentLoaded

DOMContentLoaded is raised when the initial HTML document has been parsed.
This aligns with the the document's DOMContentLoaded event in HTML.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2, [CoreWebView2DOMContentLoadedEventArgs](corewebview2domcontentloadedeventargs.md)&gt;

### DocumentTitleChanged

DocumentTitleChanged is raised when the [CoreWebView2.DocumentTitle](corewebview2.md#documenttitle) property changes and may be raised before or after the [CoreWebView2.NavigationCompleted](corewebview2.md#navigationcompleted) event.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2, Object&gt;

### DownloadStarting

DownloadStarting is raised when a download has begun, blocking the default download dialog, but not blocking the progress of the download.
The host can choose to cancel a download, change the result file path, and hide the default download dialog. If download is not handled or canceled, the download is saved to the default path after the event completes with default download dialog shown.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2, [CoreWebView2DownloadStartingEventArgs](corewebview2downloadstartingeventargs.md)&gt;

### FaviconChanged

Raised when the Favicon has changed. This can include when a new page is loaded and thus by default no icon is set or the icon is set for the page by DOM or JavaScript.
The first argument is the Webview2 which saw the changed Favicon and the second is null.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2, Object&gt;

### FrameCreated

FrameCreated is raised when a new iframe is created. Handle this event to get access to [CoreWebView2Frame](corewebview2frame.md) objects.
Use the [CoreWebView2Frame.Destroyed](corewebview2frame.md#destroyed) to listen for when this iframe goes away.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2, [CoreWebView2FrameCreatedEventArgs](corewebview2framecreatedeventargs.md)&gt;

### FrameNavigationCompleted

FrameNavigationCompleted is raised when a child frame has completely loaded (`body.onload` has been raised) or loading stopped with error.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2, [CoreWebView2NavigationCompletedEventArgs](corewebview2navigationcompletedeventargs.md)&gt;

### FrameNavigationStarting

FrameNavigationStarting is raised when a child frame in the WebView requests permission to navigate to a different URI.
Redirects raise this operation as well, and the navigation id is the same as the original one. You may block corresponding navigations until the event handler returns.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2, [CoreWebView2NavigationStartingEventArgs](corewebview2navigationstartingeventargs.md)&gt;

### HistoryChanged

HistoryChanged is raised for changes to joint session history, which consists of top-level and manual frame navigations.
Use HistoryChanged to verify that the [CoreWebView2.CanGoBack](corewebview2.md#cangoback) or [CoreWebView2.CanGoForward](corewebview2.md#cangoforward) value has changed. HistoryChanged is also raised for using [CoreWebView2.GoBack](corewebview2.md#goback) or [CoreWebView2.GoForward](corewebview2.md#goforward). HistoryChanged is raised after [CoreWebView2.SourceChanged](corewebview2.md#sourcechanged) and [CoreWebView2.ContentLoading](corewebview2.md#contentloading). CanGoBack is false for navigations initiated through CoreWebView2Frame APIs if there has not yet been a user gesture.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2, Object&gt;

### IsDefaultDownloadDialogOpenChanged

Raised when the [CoreWebView2.IsDefaultDownloadDialogOpen](corewebview2.md#isdefaultdownloaddialogopen) property changes.
This event comes after the [CoreWebView2.DownloadStarting](corewebview2.md#downloadstarting) event. Setting the [CoreWebView2DownloadStartingEventArgs.Handled](corewebview2downloadstartingeventargs.md#handled) property disables the default download dialog and ensures that this event is never raised.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2, Object&gt;

### IsDocumentPlayingAudioChanged

IsDocumentPlayingAudioChanged is raised when document starts or stops playing audio.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2, Object&gt;

### IsMutedChanged

IsMutedChanged is raised when the mute state changes.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2, Object&gt;

### LaunchingExternalUriScheme

LaunchingExternalUriScheme is raised when a navigation request is made to a URI scheme that is registered with the OS.
The [CoreWebView2.LaunchingExternalUriScheme](corewebview2.md#launchingexternalurischeme) event handler may suppress the default dialog or replace the default dialog with a custom dialog.
If a CoreWebView2Deferral (unresolved reference) is not taken on the event args, the external URI scheme launch is blocked until the event handler returns.
If a deferral is taken, the external URI scheme launch is blocked until the CoreWebView2Deferral (unresolved reference) is completed.
The host also has the option to cancel the URI scheme launch.

The [CoreWebView2.NavigationStarting](corewebview2.md#navigationstarting) and [CoreWebView2.NavigationCompleted](corewebview2.md#navigationcompleted) events will be raised,
regardless of whether the [CoreWebView2NavigationStartingEventArgs.Cancel](corewebview2navigationstartingeventargs.md#cancel) property is set to `true` or
`false`.
The [CoreWebView2.NavigationCompleted](corewebview2.md#navigationcompleted) event will be raised with the [CoreWebView2LaunchingExternalUriSchemeEventArgs.IsSuccess](corewebview2launchingexternalurischemeeventargs.md#issuccess) property set to `false` and the [CoreWebView2NavigationCompletedEventArgs.WebErrorStatus](corewebview2navigationcompletedeventargs.md#weberrorstatus) property set to [CoreWebView2WebErrorStatus.ConnectionAborted](corewebview2weberrorstatus.md#connectionaborted) regardless of whether the host sets the [CoreWebView2LaunchingExternalUriSchemeEventArgs.Cancel](corewebview2launchingexternalurischemeeventargs.md#cancel) property on the
<see cref="CoreWebView2LaunchingExternalUriSchemeEventArgs">.
The [CoreWebView2.SourceChanged](corewebview2.md#sourcechanged), [CoreWebView2.ContentLoading](corewebview2.md#contentloading) and [CoreWebView2.HistoryChanged](corewebview2.md#historychanged) events will not be raised for this navigation to the external URI scheme regardless of the [CoreWebView2NavigationStartingEventArgs.Cancel](corewebview2navigationstartingeventargs.md#cancel) property.
The [CoreWebView2.LaunchingExternalUriScheme](corewebview2.md#launchingexternalurischeme) event will be raised after the [CoreWebView2.NavigationStarting](corewebview2.md#navigationstarting) event and before the [CoreWebView2.NavigationCompleted](corewebview2.md#navigationcompleted) event.

The default [CoreWebView2Settings](corewebview2settings.md) will also be updated upon navigation to an external URI scheme.
If a setting on the [CoreWebView2Settings](corewebview2settings.md) interface has been changed, navigating to an external URI scheme will trigger the [CoreWebView2Settings](corewebview2settings.md) to update.

The WebView2 may not display the default dialog based on user settings, browser settings, and whether the origin is determined as a [trustworthy origin](https://w3c.github.io/webappsec-secure-contexts#potentially-trustworthy-origin); however, the event will still be raised.
If the request is initiated by a cross-origin frame without a user gesture, the request will be blocked and the `LaunchingExternalUriScheme` event will not be raised.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2, [CoreWebView2LaunchingExternalUriSchemeEventArgs](corewebview2launchingexternalurischemeeventargs.md)&gt;

### NavigationCompleted

NavigationCompleted is raised when the WebView has completely loaded (`body.onload` has been raised) or loading stopped with error.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2, [CoreWebView2NavigationCompletedEventArgs](corewebview2navigationcompletedeventargs.md)&gt;

### NavigationStarting

NavigationStarting is raised when the WebView main frame is requesting permission to navigate to a different URI.
Redirects raise this event as well, and the navigation id is the same as the original one. You may block corresponding navigations until the event handler returns.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2, [CoreWebView2NavigationStartingEventArgs](corewebview2navigationstartingeventargs.md)&gt;

### NewWindowRequested

NewWindowRequested is raised when content inside the WebView requests to open a new window, such as through `window.open()`.
The app can pass a target WebView that is considered the opened window or mark the event as [CoreWebView2NewWindowRequestedEventArgs.Handled](corewebview2newwindowrequestedeventargs.md#handled), in which case WebView2 does not open a window.
If either `Handled` or [CoreWebView2NewWindowRequestedEventArgs.NewWindow](corewebview2newwindowrequestedeventargs.md#newwindow) properties are not set, the target content will be opened on a popup window.
If a deferral is not taken on the event args, scripts that resulted in the new window that are requested are blocked until the event handler returns. If a deferral is taken, then scripts are blocked until the deferral is completed.

On Hololens 2, if the [CoreWebView2NewWindowRequestedEventArgs.NewWindow](corewebview2newwindowrequestedeventargs.md#newwindow) property is not set and the [CoreWebView2NewWindowRequestedEventArgs.Handled](corewebview2newwindowrequestedeventargs.md#handled) property is not set to `true`, the WebView2 will navigate to the [CoreWebView2NewWindowRequestedEventArgs.Uri](corewebview2newwindowrequestedeventargs.md#uri).
If either of these properties are set, the WebView2 will not navigate to the [CoreWebView2NewWindowRequestedEventArgs.Uri](corewebview2newwindowrequestedeventargs.md#uri) and the the [CoreWebView2.NewWindowRequested](corewebview2.md#newwindowrequested) event will continue as normal.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2, [CoreWebView2NewWindowRequestedEventArgs](corewebview2newwindowrequestedeventargs.md)&gt;

### PermissionRequested

PermissionRequested is raised when content in a WebView requests permission to access some privileged resources.
If a deferral is not taken on the event args, the subsequent scripts are blocked until the event handler returns. If a deferral is taken, the scripts are blocked until the deferral is completed.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2, [CoreWebView2PermissionRequestedEventArgs](corewebview2permissionrequestedeventargs.md)&gt;

### ProcessFailed

ProcessFailed is raised when a WebView process ends unexpectedly or becomes unresponsive.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2, [CoreWebView2ProcessFailedEventArgs](corewebview2processfailedeventargs.md)&gt;

### ScriptDialogOpening

ScriptDialogOpening is raised when a JavaScript dialog (`alert`, `confirm`, `prompt`, or `beforeunload`) displays for the WebView.
This event only is raised if the [CoreWebView2Settings.AreDefaultScriptDialogsEnabled](corewebview2settings.md#aredefaultscriptdialogsenabled) property is set to `false`. This event suppresses dialogs or replaces default dialogs with custom dialogs.

If a deferral is not taken on the event args, the subsequent scripts are blocked until the event handler returns. If a deferral is taken, the scripts are blocked until the deferral is completed.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2, [CoreWebView2ScriptDialogOpeningEventArgs](corewebview2scriptdialogopeningeventargs.md)&gt;

### ServerCertificateErrorDetected

The ServerCertificateErrorDetected event is raised when the WebView2 cannot verify server's digital certificate while loading a web page.
This event will raise for all web resources and follows the [CoreWebView2.WebResourceRequested](corewebview2.md#webresourcerequested) event.

If you don't handle the event, WebView2 will show the default TLS interstitial error page to the user for navigations, and for non-navigations the web request is cancelled.

Note that WebView2 before raising `ServerCertificateErrorDetected` raises a [CoreWebView2.NavigationCompleted](corewebview2.md#navigationcompleted) event with [CoreWebView2NavigationCompletedEventArgs.IsSuccess](corewebview2navigationcompletedeventargs.md#issuccess) as FALSE and any of the below WebErrorStatuses that indicate a certificate failure.

- [CoreWebView2WebErrorStatus](corewebview2weberrorstatus.md).CertificateCommonNameIsIncorrect
- [CoreWebView2WebErrorStatus](corewebview2weberrorstatus.md).CertificateExpired
- [CoreWebView2WebErrorStatus](corewebview2weberrorstatus.md).ClientCertificateContainsErrors
- [CoreWebView2WebErrorStatus](corewebview2weberrorstatus.md).CertificateRevoked
- [CoreWebView2WebErrorStatus](corewebview2weberrorstatus.md).CertificateIsInvalid

For more details see [CoreWebView2NavigationCompletedEventArgs.IsSuccess](corewebview2navigationcompletedeventargs.md#issuccess) and handle ServerCertificateErrorDetected event or show the default TLS interstitial error page to the user according to the app needs.

WebView2 caches the response when action is [CoreWebView2ServerCertificateErrorAction](corewebview2servercertificateerroraction.md).AlwaysAllow for the RequestUri's host and the server certificate in the session and the [CoreWebView2.ServerCertificateErrorDetected](corewebview2.md#servercertificateerrordetected) event won't be raised again.

To raise the event again you must clear the cache using [CoreWebView2.ClearServerCertificateErrorActionsAsync](corewebview2.md#clearservercertificateerroractionsasync).

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2, [CoreWebView2ServerCertificateErrorDetectedEventArgs](corewebview2servercertificateerrordetectedeventargs.md)&gt;

### SourceChanged

SourceChanged is raised when the [CoreWebView2.Source](corewebview2.md#source) property changes.
SourceChanged is raised when navigating to a different site or fragment navigations. It is not raised for other types of navigations such as page refreshes or `history.pushState` with the same URL as the current page. This event is raised before [CoreWebView2.ContentLoading](corewebview2.md#contentloading) for navigation to a new document.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2, [CoreWebView2SourceChangedEventArgs](corewebview2sourcechangedeventargs.md)&gt;

### StatusBarTextChanged

StatusBarTextChanged event is raised when the text in the [Window.statusbar](https://developer.mozilla.org/docs/Web/API/Window/statusbar) changes. When the event is fired use the property [CoreWebView2.StatusBarText](corewebview2.md#statusbartext) to get the current statusbar text.
Events which cause causes can be anything from hover, url events, and others. There is not a finite list on how to cause the statusbar to change.
The developer must create the status bar and set the text.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2, Object&gt;

### WebMessageReceived

WebMessageReceived is raised when the [CoreWebView2Settings.IsWebMessageEnabled](corewebview2settings.md#iswebmessageenabled) setting is set and the top-level document of the WebView runs `window.chrome.webview.postMessage` or `window.chrome.webview.postMessageWithAdditionalObjects`.
The `postMessage` function is `void postMessage(object)` where object is any object supported by JSON conversion.
When `postMessage` is called, the handler's Invoke method will be called with the `object` parameter `postMessage` converted to a JSON string.
If the same page calls `postMessage` multiple times, the corresponding `WebMessageReceived` events are guaranteed to be fired in the same order. However, if multiple frames call `postMessage`, there is no guaranteed order. In addition, `WebMessageReceived` events caused by calls to `postMessage` are not guaranteed to be sequenced with events caused by DOM APIs. For example, if the page runs
<code>
chrome.webview.postMessage("message");
window.open();
then the [CoreWebView2.NewWindowRequested](corewebview2.md#newwindowrequested) event might be fired before the `WebMessageReceived` event. If you need the `WebMessageReceived` event to happen before anything else, then in the `WebMessageReceived` handler you can post a message back to the page and have the page wait until it receives that message before continuing.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2, [CoreWebView2WebMessageReceivedEventArgs](corewebview2webmessagereceivedeventargs.md)&gt;

### WebResourceRequested

WebResourceRequested is raised when the WebView is performing a URL request to a matching URL and resource context filter that was added with [CoreWebView2.AddWebResourceRequestedFilter](corewebview2.md#addwebresourcerequestedfilter).
At least one filter must be added for the event to be raised.
The web resource requested may be blocked until the event handler returns if a deferral is not taken on the event args. If a deferral is taken, then the web resource requested is blocked until the deferral is completed.

If this event is subscribed in the [CoreWebView2.NewWindowRequested](corewebview2.md#newwindowrequested) handler it should be called after the new window is set. For more details see [CoreWebView2NewWindowRequestedEventArgs.NewWindow](corewebview2newwindowrequestedeventargs.md#newwindow).

Currently this only supports file, http, and https URI schemes.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2, [CoreWebView2WebResourceRequestedEventArgs](corewebview2webresourcerequestedeventargs.md)&gt;

### WebResourceResponseReceived

WebResourceResponseReceived is raised when the WebView receives the response for a request for a web resource (any URI resolution performed by the WebView; such as HTTP/HTTPS, file and data requests from redirects, navigations, declarations in HTML, implicit Favicon lookups, and fetch API usage in the document).
The host app can use this event to view the actual request and response for a web resource. There is no guarantee about the order in which the WebView processes the response and the host app's handler runs. The app's handler will not block the WebView from processing the response.
The event args include the [CoreWebView2WebResourceRequest](corewebview2webresourcerequest.md) as sent by the wire and [CoreWebView2WebResourceResponse](corewebview2webresourceresponse.md) received, including any additional headers added by the network stack that were not be included as part of the associated [CoreWebView2.WebResourceRequested](corewebview2.md#webresourcerequested) event, such as Authentication headers.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2, [CoreWebView2WebResourceResponseReceivedEventArgs](corewebview2webresourceresponsereceivedeventargs.md)&gt;

### WindowCloseRequested

WindowCloseRequested is raised when content inside the WebView requested to close the window, such as after `window.close()` is run.
The app should close the WebView and related app window if that makes sense to the app.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2, Object&gt;



## Referenced by

- [CoreWebView2Controller](corewebview2controller.md)
- [CoreWebView2DevToolsProtocolEventReceiver](corewebview2devtoolsprotocoleventreceiver.md)
- [CoreWebView2NewWindowRequestedEventArgs](corewebview2newwindowrequestedeventargs.md)
