---
description: CoreWebView2Frame provides direct access to the iframes information and handling.
title: CoreWebView2Frame
ms.date: 09/21/2021
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2Frame
---

# CoreWebView2Frame Class



CoreWebView2Frame provides direct access to the iframes information and handling.

## Summary

Members|Description
--|--
[Name](#name) | The name of the iframe from the iframe html tag declaring it.
[ExecuteScriptAsync](#executescriptasync) | Runs JavaScript code from the `javaScript` parameter in the current frame.
[IsDestroyed](#isdestroyed) | Check whether a frame is destroyed. Returns true during the [CoreWebView2Frame.Destroyed](corewebview2frame.md#destroyed) event.
[RemoveHostObjectFromScript](#removehostobjectfromscript) | Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the iframe.
[ContentLoading](#contentloading) | ContentLoading is raised before any content is loaded, including scripts added with [CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync](corewebview2.md#addscripttoexecuteondocumentcreatedasync). ContentLoading is not raised if a same page navigation occurs.
[DOMContentLoaded](#domcontentloaded) | DOMContentLoaded is raised when the initial HTML document has been parsed.
[Destroyed](#destroyed) | Destroyed event is raised when the iframe corresponding to this [CoreWebView2Frame](corewebview2frame.md) object is removed or the document containing that iframe is destroyed.
[NameChanged](#namechanged) | NameChanged is raised when the iframe changes its `window.name` property.
[NavigationCompleted](#navigationcompleted) | NavigationCompleted is raised when the current frame has completely loaded (`body.onload` has been raised) or loading stopped with error.
[NavigationStarting](#navigationstarting) | NavigationStarting is raised when the current frame is requesting permission to navigate to a different URI.

## Properties

### Name

> readonly  string Name

The name of the iframe from the iframe html tag declaring it.



## Methods

### ExecuteScriptAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;string&gt; ExecuteScriptAsync(string javaScript)

Runs JavaScript code from the `javaScript` parameter in the current frame.
A function that has no explicit return value returns `undefined`. If the script that was run throws an unhandled exception, then the result is also `null`. This method is applied asynchronously.
If the method is run before [CoreWebView2Frame.ContentLoading](corewebview2frame.md#contentloading), the script will not be executed and the JSON `null` will be returned.
This operation works even if [CoreWebView2Settings.IsScriptEnabled](corewebview2settings.md#isscriptenabled) is set to `false`.



### IsDestroyed

> int IsDestroyed()

Check whether a frame is destroyed. Returns true during the [CoreWebView2Frame.Destroyed](corewebview2frame.md#destroyed) event.



### RemoveHostObjectFromScript

> void RemoveHostObjectFromScript(string name)

Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the iframe.
While new access attempts are denied, if the object is already obtained by JavaScript code in the iframe, the JavaScript code continues to have access to that object. Calling this method for a name that is already removed or was never added fails. If the iframe is destroyed this method will return fail also.




## Events

### ContentLoading

ContentLoading is raised before any content is loaded, including scripts added with [CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync](corewebview2.md#addscripttoexecuteondocumentcreatedasync). ContentLoading is not raised if a same page navigation occurs.
This operation follows the [CoreWebView2Frame.NavigationStarting](corewebview2frame.md#navigationstarting) event and precedes the [CoreWebView2Frame.DOMContentLoaded](corewebview2frame.md#domcontentloaded) and [CoreWebView2Frame.NavigationCompleted](corewebview2frame.md#navigationcompleted) events.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2Frame](corewebview2frame.md), [CoreWebView2ContentLoadingEventArgs](corewebview2contentloadingeventargs.md)&gt;

### DOMContentLoaded

DOMContentLoaded is raised when the initial HTML document has been parsed.
This aligns with the the document's `DOMContentLoaded` event in HTML.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2Frame](corewebview2frame.md), [CoreWebView2DOMContentLoadedEventArgs](corewebview2domcontentloadedeventargs.md)&gt;

### Destroyed

Destroyed event is raised when the iframe corresponding to this [CoreWebView2Frame](corewebview2frame.md) object is removed or the document containing that iframe is destroyed.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2Frame](corewebview2frame.md), Object&gt;

### NameChanged

NameChanged is raised when the iframe changes its `window.name` property.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2Frame](corewebview2frame.md), Object&gt;

### NavigationCompleted

NavigationCompleted is raised when the current frame has completely loaded (`body.onload` has been raised) or loading stopped with error.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2Frame](corewebview2frame.md), [CoreWebView2NavigationCompletedEventArgs](corewebview2navigationcompletedeventargs.md)&gt;

### NavigationStarting

NavigationStarting is raised when the current frame is requesting permission to navigate to a different URI.
A frame navigation will raise a [CoreWebView2Frame.NavigationStarting](corewebview2frame.md#navigationstarting) event and a [CoreWebView2.FrameNavigationStarting](corewebview2.md#framenavigationstarting) event. All of the [CoreWebView2.FrameNavigationStarting](corewebview2.md#framenavigationstarting) event handlers will be run before the [CoreWebView2Frame.NavigationStarting](corewebview2frame.md#navigationstarting) event handlers. All of the event handlers share a common [CoreWebView2NavigationStartingEventArgs](corewebview2navigationstartingeventargs.md) object. Whichever event handler is last to change the [CoreWebView2NavigationStartingEventArgs.Cancel](corewebview2navigationstartingeventargs.md#cancel) property will decide if the frame navigation will be cancelled.
Redirects raise this event as well, and the navigation id is the same as the original one. You may block corresponding navigations until the event handler returns.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2Frame](corewebview2frame.md), [CoreWebView2NavigationStartingEventArgs](corewebview2navigationstartingeventargs.md)&gt;



## Referenced by

- [CoreWebView2FrameCreatedEventArgs](corewebview2framecreatedeventargs.md)
