---
description: Defines properties that enable, disable, or modify WebView features.
title: CoreWebView2Settings
ms.date: 07/27/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2Settings
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2Settings
- CoreWebView2Settings.AreBrowserAcceleratorKeysEnabled
- CoreWebView2Settings.AreDefaultContextMenusEnabled
- CoreWebView2Settings.AreDefaultScriptDialogsEnabled
- CoreWebView2Settings.AreDevToolsEnabled
- CoreWebView2Settings.AreHostObjectsAllowed
- CoreWebView2Settings.HiddenPdfToolbarItems
- CoreWebView2Settings.HostObjectDispatchAdapter
- CoreWebView2Settings.IsBuiltInErrorPageEnabled
- CoreWebView2Settings.IsGeneralAutofillEnabled
- CoreWebView2Settings.IsPasswordAutosaveEnabled
- CoreWebView2Settings.IsPinchZoomEnabled
- CoreWebView2Settings.IsReputationCheckingRequired
- CoreWebView2Settings.IsScriptEnabled
- CoreWebView2Settings.IsStatusBarEnabled
- CoreWebView2Settings.IsSwipeNavigationEnabled
- CoreWebView2Settings.IsWebMessageEnabled
- CoreWebView2Settings.IsZoomControlEnabled
- CoreWebView2Settings.UserAgent
- CoreWebView2Settings.get_AreBrowserAcceleratorKeysEnabled
- CoreWebView2Settings.get_AreDefaultContextMenusEnabled
- CoreWebView2Settings.get_AreDefaultScriptDialogsEnabled
- CoreWebView2Settings.get_AreDevToolsEnabled
- CoreWebView2Settings.get_AreHostObjectsAllowed
- CoreWebView2Settings.get_HiddenPdfToolbarItems
- CoreWebView2Settings.get_HostObjectDispatchAdapter
- CoreWebView2Settings.get_IsBuiltInErrorPageEnabled
- CoreWebView2Settings.get_IsGeneralAutofillEnabled
- CoreWebView2Settings.get_IsPasswordAutosaveEnabled
- CoreWebView2Settings.get_IsPinchZoomEnabled
- CoreWebView2Settings.get_IsReputationCheckingRequired
- CoreWebView2Settings.get_IsScriptEnabled
- CoreWebView2Settings.get_IsStatusBarEnabled
- CoreWebView2Settings.get_IsSwipeNavigationEnabled
- CoreWebView2Settings.get_IsWebMessageEnabled
- CoreWebView2Settings.get_IsZoomControlEnabled
- CoreWebView2Settings.get_UserAgent
- CoreWebView2Settings.put_AreBrowserAcceleratorKeysEnabled
- CoreWebView2Settings.put_AreDefaultContextMenusEnabled
- CoreWebView2Settings.put_AreDefaultScriptDialogsEnabled
- CoreWebView2Settings.put_AreDevToolsEnabled
- CoreWebView2Settings.put_AreHostObjectsAllowed
- CoreWebView2Settings.put_HiddenPdfToolbarItems
- CoreWebView2Settings.put_HostObjectDispatchAdapter
- CoreWebView2Settings.put_IsBuiltInErrorPageEnabled
- CoreWebView2Settings.put_IsGeneralAutofillEnabled
- CoreWebView2Settings.put_IsPasswordAutosaveEnabled
- CoreWebView2Settings.put_IsPinchZoomEnabled
- CoreWebView2Settings.put_IsReputationCheckingRequired
- CoreWebView2Settings.put_IsScriptEnabled
- CoreWebView2Settings.put_IsStatusBarEnabled
- CoreWebView2Settings.put_IsSwipeNavigationEnabled
- CoreWebView2Settings.put_IsWebMessageEnabled
- CoreWebView2Settings.put_IsZoomControlEnabled
- CoreWebView2Settings.put_UserAgent
---

# CoreWebView2Settings Class



Defines properties that enable, disable, or modify WebView features.
Changes to [CoreWebView2Settings.IsGeneralAutofillEnabled](corewebview2settings.md#isgeneralautofillenabled) and [CoreWebView2Settings.IsPasswordAutosaveEnabled](corewebview2settings.md#ispasswordautosaveenabled) will take effect immediately, while other setting changes made after [CoreWebView2.NavigationStarting](corewebview2.md#navigationstarting) event do not apply until the next top-level navigation.

## Summary

Members|Description
--|--
[AreBrowserAcceleratorKeysEnabled](#arebrowseracceleratorkeysenabled) | Determines whether browser-specific accelerator keys are enabled.
[AreDefaultContextMenusEnabled](#aredefaultcontextmenusenabled) | Determines whether the default context menus are shown to the user in WebView.
[AreDefaultScriptDialogsEnabled](#aredefaultscriptdialogsenabled) | Determines whether WebView renders the default JavaScript dialog box.
[AreDevToolsEnabled](#aredevtoolsenabled) | Determines whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.
[AreHostObjectsAllowed](#arehostobjectsallowed) | Determines whether host objects are accessible from the page in WebView.
[HiddenPdfToolbarItems](#hiddenpdftoolbaritems) | Used to customize the PDF toolbar items.
[HostObjectDispatchAdapter](#hostobjectdispatchadapter) | The default adapter to be used when passing IInspectable objects to [CoreWebView2.AddHostObjectToScript](corewebview2.md#addhostobjecttoscript).
[IsBuiltInErrorPageEnabled](#isbuiltinerrorpageenabled) | Determines whether to disable built in error page for navigation failure and render process failure.
[IsGeneralAutofillEnabled](#isgeneralautofillenabled) | Determines whether general form information will be saved and autofilled.
[IsPasswordAutosaveEnabled](#ispasswordautosaveenabled) | Determines whether password information will be autosaved.
[IsPinchZoomEnabled](#ispinchzoomenabled) | Determines the ability of the end users to use pinching motions on touch input enabled devices to scale the web content in the WebView2.
[IsReputationCheckingRequired](#isreputationcheckingrequired) | Determines whether SmartScreen is enabled when visiting web pages
[IsScriptEnabled](#isscriptenabled) | Determines whether running JavaScript is enabled in all future navigations in the WebView.
[IsStatusBarEnabled](#isstatusbarenabled) | Determines whether the status bar is displayed.
[IsSwipeNavigationEnabled](#isswipenavigationenabled) | Determines whether the end user to use swiping gesture on touch input enabled devices to navigate in WebView2.
[IsWebMessageEnabled](#iswebmessageenabled) | Determines whether communication from the host to the top-level HTML document of the WebView is allowed.
[IsZoomControlEnabled](#iszoomcontrolenabled) | Determines whether the user is able to impact the zoom of the WebView.
[UserAgent](#useragent) | Determines WebView2's User Agent.

## Properties

### AreBrowserAcceleratorKeysEnabled

>  bool AreBrowserAcceleratorKeysEnabled

Determines whether browser-specific accelerator keys are enabled.
When this setting is set to false, it disables all accelerator keys that access
features specific to a web browser, including but not limited to:

- Ctrl+F and F3 for Find on Page
- Ctrl+P for Print
- Ctrl+R and F5 for Reload
- Ctrl+Plus and Ctrl+Minus for zooming
- Ctrl+Shift-C and F12 for DevTools
- Special keys for browser functions, such as Back, Forward, and Search

It does not disable accelerator keys related to movement and text editing, such
as:

- Home, End, Page Up, and Page Down
- Ctrl+X, Ctrl+C, Ctrl+V
- Ctrl+A for Select All
- Ctrl+Z for Undo

Those accelerator keys will always be enabled unless they are handled in the [CoreWebView2Controller.AcceleratorKeyPressed](corewebview2controller.md#acceleratorkeypressed) event.

This setting has no effect on the [CoreWebView2Controller.AcceleratorKeyPressed](corewebview2controller.md#acceleratorkeypressed) event. The event
will be fired for all accelerator keys, whether they are enabled or not.

The default value of `AreBrowserAcceleratorKeysEnabled` is true.

### AreDefaultContextMenusEnabled

>  bool AreDefaultContextMenusEnabled

Determines whether the default context menus are shown to the user in WebView.
The default value is `true`.

### AreDefaultScriptDialogsEnabled

>  bool AreDefaultScriptDialogsEnabled

Determines whether WebView renders the default JavaScript dialog box.
This is used when loading a new HTML document. If set to `false`, WebView does not render the default JavaScript dialog box (specifically those displayed by the JavaScript alert, confirm, prompt functions and `beforeunload` event). Instead, WebView raises [CoreWebView2.ScriptDialogOpening](corewebview2.md#scriptdialogopening) event that contains all of the information for the dialog and allow the host app to show a custom UI. The default value is `true`.

### AreDevToolsEnabled

>  bool AreDevToolsEnabled

Determines whether the user is able to use the context menu or keyboard shortcuts to open the DevTools window.
The default value is `true`.

### AreHostObjectsAllowed

>  bool AreHostObjectsAllowed

Determines whether host objects are accessible from the page in WebView.
The default value is `true`.

### HiddenPdfToolbarItems

>  [CoreWebView2PdfToolbarItems](corewebview2pdftoolbaritems.md) HiddenPdfToolbarItems

Used to customize the PDF toolbar items.
By default, it is [CoreWebView2PdfToolbarItems](corewebview2pdftoolbaritems.md).None and so it displays all of the items.
Changes to this property apply to all CoreWebView2s in the same environment and using the same profile.
Changes to this setting apply only after the next navigation.

### HostObjectDispatchAdapter

>  [ICoreWebView2DispatchAdapter](icorewebview2dispatchadapter.md) HostObjectDispatchAdapter

The default adapter to be used when passing IInspectable objects to [CoreWebView2.AddHostObjectToScript](corewebview2.md#addhostobjecttoscript).

### IsBuiltInErrorPageEnabled

>  bool IsBuiltInErrorPageEnabled

Determines whether to disable built in error page for navigation failure and render process failure.
When disabled, blank page is displayed when related error happens. The default value is `true`.

### IsGeneralAutofillEnabled

>  bool IsGeneralAutofillEnabled

Determines whether general form information will be saved and autofilled.
General autofill information includes information like names, street and email addresses, phone numbers, and arbitrary input. This excludes password information. When disabled, no suggestions appear, and no new information is saved.
When enabled, information is saved, suggestions appear, and clicking on one will populate the form fields. The default value is `true`. It will apply immediately after setting.
This property has the same value as [CoreWebView2Profile.IsGeneralAutofillEnabled](corewebview2profile.md#isgeneralautofillenabled), and changing one will change the other. And all WebView2s that created with the same [CoreWebView2Profile](corewebview2profile.md) will share the same value for this property, so for the WebView2s with the same profile, their [CoreWebView2Settings.IsGeneralAutofillEnabled](corewebview2settings.md#isgeneralautofillenabled) and [CoreWebView2Profile.IsGeneralAutofillEnabled](corewebview2profile.md#isgeneralautofillenabled) will always have the same value.

### IsPasswordAutosaveEnabled

>  bool IsPasswordAutosaveEnabled

Determines whether password information will be autosaved.
When disabled, no new password data is saved and no Save/Update Password prompts are displayed. However, if there was password data already saved before disabling this setting, then that password information is auto-populated, suggestions are shown and clicking on one will populate the fields.
When enabled, password information is auto-populated, suggestions are shown and clicking on one will populate the fields, new data is saved, and a Save/Update Password prompt is displayed. The default value is `false`. It will apply immediately after setting.
This property has the same value as [CoreWebView2Profile.IsPasswordAutosaveEnabled](corewebview2profile.md#ispasswordautosaveenabled), and changing one will change the other. All WebView2s with the same [CoreWebView2Profile](corewebview2profile.md) will share the same value for this property, so for the WebView2s with the same profile, their [CoreWebView2Settings.IsPasswordAutosaveEnabled](corewebview2settings.md#ispasswordautosaveenabled) and [CoreWebView2Profile.IsPasswordAutosaveEnabled](corewebview2profile.md#ispasswordautosaveenabled) will always have the same value.

### IsPinchZoomEnabled

>  bool IsPinchZoomEnabled

Determines the ability of the end users to use pinching motions on touch input enabled devices to scale the web content in the WebView2.
When disabled, the end users cannot use pinching motions on touch input enabled devices to scale the web content in the WebView2. The default value is `true`.
Pinch-zoom, referred to as "Page Scale" zoom, is performed as a post-rendering step, it changes the page scale factor property and scales the surface the web page is rendered onto when user performs a pinch zooming action. It does not change the layout but rather changes the viewport and clips the web content, the content outside of the viewport isn't visible onscreen and users can't reach this content using mouse. This API only affects the Page Scale zoom and has no effect on the existing browser zoom properties ([CoreWebView2Settings.IsZoomControlEnabled](corewebview2settings.md#iszoomcontrolenabled) and [CoreWebView2Controller.ZoomFactor](corewebview2controller.md#zoomfactor)) or other end user mechanisms for zooming.

### IsReputationCheckingRequired

>  bool IsReputationCheckingRequired

Determines whether SmartScreen is enabled when visiting web pages
The default value is `true`.
IsReputationCheckingRequired is used to control whether SmartScreen is enabled or not.
SmartScreen is enabled or disabled for all CoreWebView2s using the same user data folder.
If CoreWebView2Setting.IsReputationCheckingRequired is `true` for any CoreWebView2 using the same user data folder, then SmartScreen is enabled. If CoreWebView2Setting.IsReputationCheckingRequired is `false` for all CoreWebView2 using the same user data folder, then SmartScreen is disabled.
When it is changed, the change will be applied to all WebViews using the same user data folder on the next navigation or download.
If the newly created CoreWebview2 does not set SmartScreen to `false`, when navigating(Such as Navigate(), LoadDataUrl(), ExecuteScript(), etc.), the default value will be applied to all CoreWebview2 using the same user data folder.
SmartScreen of WebView2 apps can be controlled by Windows system setting "SmartScreen for Microsoft Edge", specially, for WebView2 in Windows Store apps, SmartScreen is controlled by another Windows system setting "SmartScreen for Microsoft Store apps". When the Windows setting is enabled, the SmartScreen operates under the control of the `IsReputationCheckingRequired`. When the Windows setting is disabled, the SmartScreen will be disabled regardless of the `IsReputationCheckingRequired` value set in WebView2 apps. In other words, under this circumstance the value of `IsReputationCheckingRequired` will be saved but overridden by system setting. Upon re-enabling the Windows setting, the CoreWebview2 will reference the `IsReputationCheckingRequired` to determine the SmartScreen status.

### IsScriptEnabled

>  bool IsScriptEnabled

Determines whether running JavaScript is enabled in all future navigations in the WebView.
This only affects scripts in the document. Scripts injected with [CoreWebView2.ExecuteScriptAsync](corewebview2.md#executescriptasync) runs even if script is disabled. The default value is `true`.

### IsStatusBarEnabled

>  bool IsStatusBarEnabled

Determines whether the status bar is displayed.
The status bar is usually displayed in the lower left of the WebView and shows things such as the URI of a link when the user hovers over it and other information. The default value is `true`. The status bar UI can be altered by web content and should not be considered secure.

### IsSwipeNavigationEnabled

>  bool IsSwipeNavigationEnabled

Determines whether the end user to use swiping gesture on touch input enabled devices to navigate in WebView2.
Swiping gesture navigation on touch screen includes:

- Swipe left/right (swipe horizontally) to navigate to previous/next page in navigation history.
- Pull to refresh (swipe vertically) the current page. (This feature is currently disabled by default in the browser, to enable in WebView2, set [CoreWebView2EnvironmentOptions.AdditionalBrowserArguments](corewebview2environmentoptions.md#additionalbrowserarguments) property with `--pull-to-refresh` switch).
It defaults to `true`. When set to `false`, the end user cannot swipe to navigate or pull to refresh. This API only affects the overscrolling navigation functionality and has no effect on the scrolling interaction used to explore the web content shown in WebView2.

### IsWebMessageEnabled

>  bool IsWebMessageEnabled

Determines whether communication from the host to the top-level HTML document of the WebView is allowed.
This is used when loading a new HTML document. If set to `true`, communication from the host to the top-level HTML document of the WebView is allowed using [CoreWebView2.PostWebMessageAsJson](corewebview2.md#postwebmessageasjson), [CoreWebView2.PostWebMessageAsString](corewebview2.md#postwebmessageasstring), and message event of `window.chrome.webview`. Communication from the top-level HTML document of the WebView to the host is allowed using `window.chrome.webview.postMessage` function and the [CoreWebView2.WebMessageReceived](corewebview2.md#webmessagereceived) event. If set to `false`, then communication is disallowed. [CoreWebView2.PostWebMessageAsJson](corewebview2.md#postwebmessageasjson) and [CoreWebView2.PostWebMessageAsString](corewebview2.md#postwebmessageasstring) fail and `window.chrome.webview.postMessage` fails by throwing an instance of an Error object. The default value is `true`.

### IsZoomControlEnabled

>  bool IsZoomControlEnabled

Determines whether the user is able to impact the zoom of the WebView.
When disabled, the user is not able to zoom using Ctrl++, Ctr+-, or Ctrl+mouse wheel, but the zoom is set using [CoreWebView2Controller.ZoomFactor](corewebview2controller.md#zoomfactor) property. The default value is `true`.

### UserAgent

>  string UserAgent

Determines WebView2's User Agent.
The default value is the default User Agent of the Edge browser. This property may be overridden if the User-Agent header is set in a request. If the parameter is empty the User Agent will not be updated and the current User Agent will remain.






## Referenced by

- [CoreWebView2](corewebview2.md)
