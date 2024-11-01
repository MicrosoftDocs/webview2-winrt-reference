---
title: CoreWebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/01/2024
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2
---

# runtimeClass CoreWebView2



## Summary

Members|Description
--|--
[BrowserProcessId](#browserprocessid) | 
[CanGoBack](#cangoback) | 
[CanGoForward](#cangoforward) | 
[ContainsFullScreenElement](#containsfullscreenelement) | 
[CookieManager](#cookiemanager) | 
[CustomDataPartitionId](#customdatapartitionid) | 
[DefaultDownloadDialogCornerAlignment](#defaultdownloaddialogcorneralignment) | 
[DefaultDownloadDialogMargin](#defaultdownloaddialogmargin) | 
[DocumentTitle](#documenttitle) | 
[Environment](#environment) | 
[FaviconUri](#faviconuri) | 
[FrameId](#frameid) | 
[IsDefaultDownloadDialogOpen](#isdefaultdownloaddialogopen) | 
[IsDocumentPlayingAudio](#isdocumentplayingaudio) | 
[IsMuted](#ismuted) | 
[IsSuspended](#issuspended) | 
[MemoryUsageTargetLevel](#memoryusagetargetlevel) | 
[Profile](#profile) | 
[Settings](#settings) | 
[Source](#source) | 
[StatusBarText](#statusbartext) | 
[AddHostObjectToScript](#addhostobjecttoscript) | 
[AddScriptToExecuteOnDocumentCreatedAsync](#addscripttoexecuteondocumentcreatedasync) | 
[AddWebResourceRequestedFilter](#addwebresourcerequestedfilter) | 
[AddWebResourceRequestedFilter](#addwebresourcerequestedfilter) | 
[CallDevToolsProtocolMethodAsync](#calldevtoolsprotocolmethodasync) | 
[CallDevToolsProtocolMethodForSessionAsync](#calldevtoolsprotocolmethodforsessionasync) | 
[CapturePreviewAsync](#capturepreviewasync) | 
[ClearServerCertificateErrorActionsAsync](#clearservercertificateerroractionsasync) | 
[ClearVirtualHostNameToFolderMapping](#clearvirtualhostnametofoldermapping) | 
[CloseDefaultDownloadDialog](#closedefaultdownloaddialog) | 
[ExecuteScriptAsync](#executescriptasync) | 
[ExecuteScriptWithResultAsync](#executescriptwithresultasync) | 
[GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver) | 
[GetFaviconAsync](#getfaviconasync) | 
[GoBack](#goback) | 
[GoForward](#goforward) | 
[Navigate](#navigate) | 
[NavigateToString](#navigatetostring) | 
[NavigateWithWebResourceRequest](#navigatewithwebresourcerequest) | 
[OpenDefaultDownloadDialog](#opendefaultdownloaddialog) | 
[OpenDevToolsWindow](#opendevtoolswindow) | 
[OpenTaskManagerWindow](#opentaskmanagerwindow) | 
[PostSharedBufferToScript](#postsharedbuffertoscript) | 
[PostWebMessageAsJson](#postwebmessageasjson) | 
[PostWebMessageAsJson](#postwebmessageasjson) | 
[PostWebMessageAsString](#postwebmessageasstring) | 
[PrintAsync](#printasync) | 
[PrintToPdfAsync](#printtopdfasync) | 
[PrintToPdfStreamAsync](#printtopdfstreamasync) | 
[Reload](#reload) | 
[RemoveHostObjectFromScript](#removehostobjectfromscript) | 
[RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated) | 
[RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter) | 
[RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter) | 
[Resume](#resume) | 
[SetVirtualHostNameToFolderMapping](#setvirtualhostnametofoldermapping) | 
[ShowPrintUI](#showprintui) | 
[ShowSaveAsUIAsync](#showsaveasuiasync) | 
[Stop](#stop) | 
[TrySuspendAsync](#trysuspendasync) | 
[BasicAuthenticationRequested](#basicauthenticationrequested) | 
[ClientCertificateRequested](#clientcertificaterequested) | 
[ContainsFullScreenElementChanged](#containsfullscreenelementchanged) | 
[ContentLoading](#contentloading) | 
[ContextMenuRequested](#contextmenurequested) | 
[DOMContentLoaded](#domcontentloaded) | 
[DocumentTitleChanged](#documenttitlechanged) | 
[DownloadStarting](#downloadstarting) | 
[FaviconChanged](#faviconchanged) | 
[FrameCreated](#framecreated) | 
[FrameNavigationCompleted](#framenavigationcompleted) | 
[FrameNavigationStarting](#framenavigationstarting) | 
[HistoryChanged](#historychanged) | 
[IsDefaultDownloadDialogOpenChanged](#isdefaultdownloaddialogopenchanged) | 
[IsDocumentPlayingAudioChanged](#isdocumentplayingaudiochanged) | 
[IsMutedChanged](#ismutedchanged) | 
[LaunchingExternalUriScheme](#launchingexternalurischeme) | 
[NavigationCompleted](#navigationcompleted) | 
[NavigationStarting](#navigationstarting) | 
[NewWindowRequested](#newwindowrequested) | 
[NotificationReceived](#notificationreceived) | 
[PermissionRequested](#permissionrequested) | 
[ProcessFailed](#processfailed) | 
[SaveAsUIShowing](#saveasuishowing) | 
[SaveFileSecurityCheckStarting](#savefilesecuritycheckstarting) | 
[ScreenCaptureStarting](#screencapturestarting) | 
[ScriptDialogOpening](#scriptdialogopening) | 
[ServerCertificateErrorDetected](#servercertificateerrordetected) | 
[SourceChanged](#sourcechanged) | 
[StatusBarTextChanged](#statusbartextchanged) | 
[WebMessageReceived](#webmessagereceived) | 
[WebResourceRequested](#webresourcerequested) | 
[WebResourceResponseReceived](#webresourceresponsereceived) | 
[WindowCloseRequested](#windowcloserequested) | 

## Properties

### BrowserProcessId

> readonly  uint32_t BrowserProcessId

### CanGoBack

> readonly  bool CanGoBack

### CanGoForward

> readonly  bool CanGoForward

### ContainsFullScreenElement

> readonly  bool ContainsFullScreenElement

### CookieManager

> readonly  [CoreWebView2CookieManager](corewebview2cookiemanager.md) CookieManager

### CustomDataPartitionId

>  string CustomDataPartitionId

### DefaultDownloadDialogCornerAlignment

>  [CoreWebView2DefaultDownloadDialogCornerAlignment](corewebview2defaultdownloaddialogcorneralignment.md) DefaultDownloadDialogCornerAlignment

### DefaultDownloadDialogMargin

>  [Point](/uwp/api/Windows.Foundation.Point) DefaultDownloadDialogMargin

### DocumentTitle

> readonly  string DocumentTitle

### Environment

> readonly  [CoreWebView2Environment](corewebview2environment.md) Environment

### FaviconUri

> readonly  string FaviconUri

### FrameId

> readonly  uint32_t FrameId

### IsDefaultDownloadDialogOpen

> readonly  bool IsDefaultDownloadDialogOpen

### IsDocumentPlayingAudio

> readonly  bool IsDocumentPlayingAudio

### IsMuted

>  bool IsMuted

### IsSuspended

> readonly  bool IsSuspended

### MemoryUsageTargetLevel

>  [CoreWebView2MemoryUsageTargetLevel](corewebview2memoryusagetargetlevel.md) MemoryUsageTargetLevel

### Profile

> readonly  [CoreWebView2Profile](corewebview2profile.md) Profile

### Settings

> readonly  [CoreWebView2Settings](corewebview2settings.md) Settings

### Source

> readonly  string Source

### StatusBarText

> readonly  string StatusBarText



## Methods

### AddHostObjectToScript

> void AddHostObjectToScript(string name, Object rawObject)



### AddScriptToExecuteOnDocumentCreatedAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;string&gt; AddScriptToExecuteOnDocumentCreatedAsync(string operation)



### AddWebResourceRequestedFilter

> void AddWebResourceRequestedFilter(string uri, [CoreWebView2WebResourceContext](corewebview2webresourcecontext.md) resourceContext, [CoreWebView2WebResourceRequestSourceKinds](corewebview2webresourcerequestsourcekinds.md) requestSourceKinds)



### AddWebResourceRequestedFilter

> void AddWebResourceRequestedFilter(string uri, [CoreWebView2WebResourceContext](corewebview2webresourcecontext.md) ResourceContext)



### CallDevToolsProtocolMethodAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;string&gt; CallDevToolsProtocolMethodAsync(string operation, string methodName)



### CallDevToolsProtocolMethodForSessionAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;string&gt; CallDevToolsProtocolMethodForSessionAsync(string operation, string sessionId, string methodName)



### CapturePreviewAsync

> [IAsyncAction](/uwp/api/Windows.Foundation.IAsyncAction) CapturePreviewAsync([CoreWebView2CapturePreviewImageFormat](corewebview2capturepreviewimageformat.md) operation, [IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) imageFormat)



### ClearServerCertificateErrorActionsAsync

> [IAsyncAction](/uwp/api/Windows.Foundation.IAsyncAction) ClearServerCertificateErrorActionsAsync()



### ClearVirtualHostNameToFolderMapping

> void ClearVirtualHostNameToFolderMapping(string hostName)



### CloseDefaultDownloadDialog

> void CloseDefaultDownloadDialog()



### ExecuteScriptAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;string&gt; ExecuteScriptAsync(string operation)



### ExecuteScriptWithResultAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;[CoreWebView2ExecuteScriptResult](corewebview2executescriptresult.md)&gt; ExecuteScriptWithResultAsync(string operation)



### GetDevToolsProtocolEventReceiver

> [CoreWebView2DevToolsProtocolEventReceiver](corewebview2devtoolsprotocoleventreceiver.md) GetDevToolsProtocolEventReceiver(string eventName)



### GetFaviconAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;[IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream)&gt; GetFaviconAsync([CoreWebView2FaviconImageFormat](corewebview2faviconimageformat.md) operation)



### GoBack

> void GoBack()



### GoForward

> void GoForward()



### Navigate

> void Navigate(string uri)



### NavigateToString

> void NavigateToString(string htmlContent)



### NavigateWithWebResourceRequest

> void NavigateWithWebResourceRequest([CoreWebView2WebResourceRequest](corewebview2webresourcerequest.md) Request)



### OpenDefaultDownloadDialog

> void OpenDefaultDownloadDialog()



### OpenDevToolsWindow

> void OpenDevToolsWindow()



### OpenTaskManagerWindow

> void OpenTaskManagerWindow()



### PostSharedBufferToScript

> void PostSharedBufferToScript([CoreWebView2SharedBuffer](corewebview2sharedbuffer.md) sharedBuffer, [CoreWebView2SharedBufferAccess](corewebview2sharedbufferaccess.md) access, string additionalDataAsJson)



### PostWebMessageAsJson

> void PostWebMessageAsJson(string webMessageAsJson, [`IVectorView`](/uwp/api/Windows.Foundation.Collections.IVectorView-1)&lt;Object&gt; additionalObjects)



### PostWebMessageAsJson

> void PostWebMessageAsJson(string webMessageAsJson)



### PostWebMessageAsString

> void PostWebMessageAsString(string webMessageAsString)



### PrintAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;[CoreWebView2PrintStatus](corewebview2printstatus.md)&gt; PrintAsync([CoreWebView2PrintSettings](corewebview2printsettings.md) operation)



### PrintToPdfAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;bool&gt; PrintToPdfAsync(string operation, [CoreWebView2PrintSettings](corewebview2printsettings.md) ResultFilePath)



### PrintToPdfStreamAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;[IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream)&gt; PrintToPdfStreamAsync([CoreWebView2PrintSettings](corewebview2printsettings.md) operation)



### Reload

> void Reload()



### RemoveHostObjectFromScript

> void RemoveHostObjectFromScript(string name)



### RemoveScriptToExecuteOnDocumentCreated

> void RemoveScriptToExecuteOnDocumentCreated(string id)



### RemoveWebResourceRequestedFilter

> void RemoveWebResourceRequestedFilter(string uri, [CoreWebView2WebResourceContext](corewebview2webresourcecontext.md) resourceContext, [CoreWebView2WebResourceRequestSourceKinds](corewebview2webresourcerequestsourcekinds.md) requestSourceKinds)



### RemoveWebResourceRequestedFilter

> void RemoveWebResourceRequestedFilter(string uri, [CoreWebView2WebResourceContext](corewebview2webresourcecontext.md) ResourceContext)



### Resume

> void Resume()



### SetVirtualHostNameToFolderMapping

> void SetVirtualHostNameToFolderMapping(string hostName, string folderPath, [CoreWebView2HostResourceAccessKind](corewebview2hostresourceaccesskind.md) accessKind)



### ShowPrintUI

> void ShowPrintUI([CoreWebView2PrintDialogKind](corewebview2printdialogkind.md) printDialogKind)



### ShowSaveAsUIAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;[CoreWebView2SaveAsUIResult](corewebview2saveasuiresult.md)&gt; ShowSaveAsUIAsync()



### Stop

> void Stop()



### TrySuspendAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;bool&gt; TrySuspendAsync()




## Events

### BasicAuthenticationRequested

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2](corewebview2.md), [CoreWebView2BasicAuthenticationRequestedEventArgs](corewebview2basicauthenticationrequestedeventargs.md)&gt;

### ClientCertificateRequested

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2](corewebview2.md), [CoreWebView2ClientCertificateRequestedEventArgs](corewebview2clientcertificaterequestedeventargs.md)&gt;

### ContainsFullScreenElementChanged

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2](corewebview2.md), Object&gt;

### ContentLoading

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2](corewebview2.md), [CoreWebView2ContentLoadingEventArgs](corewebview2contentloadingeventargs.md)&gt;

### ContextMenuRequested

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2](corewebview2.md), [CoreWebView2ContextMenuRequestedEventArgs](corewebview2contextmenurequestedeventargs.md)&gt;

### DOMContentLoaded

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2](corewebview2.md), [CoreWebView2DOMContentLoadedEventArgs](corewebview2domcontentloadedeventargs.md)&gt;

### DocumentTitleChanged

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2](corewebview2.md), Object&gt;

### DownloadStarting

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2](corewebview2.md), [CoreWebView2DownloadStartingEventArgs](corewebview2downloadstartingeventargs.md)&gt;

### FaviconChanged

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2](corewebview2.md), Object&gt;

### FrameCreated

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2](corewebview2.md), [CoreWebView2FrameCreatedEventArgs](corewebview2framecreatedeventargs.md)&gt;

### FrameNavigationCompleted

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2](corewebview2.md), [CoreWebView2NavigationCompletedEventArgs](corewebview2navigationcompletedeventargs.md)&gt;

### FrameNavigationStarting

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2](corewebview2.md), [CoreWebView2NavigationStartingEventArgs](corewebview2navigationstartingeventargs.md)&gt;

### HistoryChanged

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2](corewebview2.md), Object&gt;

### IsDefaultDownloadDialogOpenChanged

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2](corewebview2.md), Object&gt;

### IsDocumentPlayingAudioChanged

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2](corewebview2.md), Object&gt;

### IsMutedChanged

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2](corewebview2.md), Object&gt;

### LaunchingExternalUriScheme

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2](corewebview2.md), [CoreWebView2LaunchingExternalUriSchemeEventArgs](corewebview2launchingexternalurischemeeventargs.md)&gt;

### NavigationCompleted

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2](corewebview2.md), [CoreWebView2NavigationCompletedEventArgs](corewebview2navigationcompletedeventargs.md)&gt;

### NavigationStarting

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2](corewebview2.md), [CoreWebView2NavigationStartingEventArgs](corewebview2navigationstartingeventargs.md)&gt;

### NewWindowRequested

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2](corewebview2.md), [CoreWebView2NewWindowRequestedEventArgs](corewebview2newwindowrequestedeventargs.md)&gt;

### NotificationReceived

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2](corewebview2.md), [CoreWebView2NotificationReceivedEventArgs](corewebview2notificationreceivedeventargs.md)&gt;

### PermissionRequested

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2](corewebview2.md), [CoreWebView2PermissionRequestedEventArgs](corewebview2permissionrequestedeventargs.md)&gt;

### ProcessFailed

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2](corewebview2.md), [CoreWebView2ProcessFailedEventArgs](corewebview2processfailedeventargs.md)&gt;

### SaveAsUIShowing

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2](corewebview2.md), [CoreWebView2SaveAsUIShowingEventArgs](corewebview2saveasuishowingeventargs.md)&gt;

### SaveFileSecurityCheckStarting

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2](corewebview2.md), [CoreWebView2SaveFileSecurityCheckStartingEventArgs](corewebview2savefilesecuritycheckstartingeventargs.md)&gt;

### ScreenCaptureStarting

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2](corewebview2.md), [CoreWebView2ScreenCaptureStartingEventArgs](corewebview2screencapturestartingeventargs.md)&gt;

### ScriptDialogOpening

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2](corewebview2.md), [CoreWebView2ScriptDialogOpeningEventArgs](corewebview2scriptdialogopeningeventargs.md)&gt;

### ServerCertificateErrorDetected

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2](corewebview2.md), [CoreWebView2ServerCertificateErrorDetectedEventArgs](corewebview2servercertificateerrordetectedeventargs.md)&gt;

### SourceChanged

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2](corewebview2.md), [CoreWebView2SourceChangedEventArgs](corewebview2sourcechangedeventargs.md)&gt;

### StatusBarTextChanged

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2](corewebview2.md), Object&gt;

### WebMessageReceived

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2](corewebview2.md), [CoreWebView2WebMessageReceivedEventArgs](corewebview2webmessagereceivedeventargs.md)&gt;

### WebResourceRequested

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2](corewebview2.md), [CoreWebView2WebResourceRequestedEventArgs](corewebview2webresourcerequestedeventargs.md)&gt;

### WebResourceResponseReceived

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2](corewebview2.md), [CoreWebView2WebResourceResponseReceivedEventArgs](corewebview2webresourceresponsereceivedeventargs.md)&gt;

### WindowCloseRequested

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2](corewebview2.md), Object&gt;



## Referenced by

- [CoreWebView2Controller](corewebview2controller.md)
- [CoreWebView2DevToolsProtocolEventReceiver](corewebview2devtoolsprotocoleventreceiver.md)
- [CoreWebView2NewWindowRequestedEventArgs](corewebview2newwindowrequestedeventargs.md)
