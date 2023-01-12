---
description: CoreWebView2Frame provides direct access to the iframes information and handling. You can get a CoreWebView2Frame by handling the CoreWebView2.FrameCreated event.
title: CoreWebView2Frame
ms.date: 01/17/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2Frame
---

# CoreWebView2Frame Class



CoreWebView2Frame provides direct access to the iframes information and handling. You can get a CoreWebView2Frame by handling the [CoreWebView2.FrameCreated](corewebview2.md#framecreated) event.

## Summary

Members|Description
--|--
[Name](#name) | The name of the iframe from the iframe html tag declaring it.
[ExecuteScriptAsync](#executescriptasync) | Runs JavaScript code from the `javaScript` parameter in the current frame.
[IsDestroyed](#isdestroyed) | Check whether a frame is destroyed. Returns true during the [CoreWebView2Frame.Destroyed](corewebview2frame.md#destroyed) event.
[PostWebMessageAsJson](#postwebmessageasjson) | Posts the specified `webMessageAsJson` to the current frame.
[PostWebMessageAsString](#postwebmessageasstring) | Posts a message that is a simple string rather than a JSON string representation of a JavaScript object.
[RemoveHostObjectFromScript](#removehostobjectfromscript) | Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the iframe.
[ContentLoading](#contentloading) | ContentLoading is raised before any content is loaded, including scripts added with [CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync](corewebview2.md#addscripttoexecuteondocumentcreatedasync). ContentLoading is not raised if a same page navigation occurs.
[DOMContentLoaded](#domcontentloaded) | DOMContentLoaded is raised when the initial HTML document has been parsed.
[Destroyed](#destroyed) | Destroyed event is raised when the iframe corresponding to this CoreWebView2Frame object is removed or the document containing that iframe is destroyed.
[NameChanged](#namechanged) | NameChanged is raised when the iframe changes its `window.name` property.
[NavigationCompleted](#navigationcompleted) | NavigationCompleted is raised when the current frame has completely loaded (`body.onload` has been raised) or loading stopped with error.
[NavigationStarting](#navigationstarting) | NavigationStarting is raised when the current frame is requesting permission to navigate to a different URI.
[PermissionRequested](#permissionrequested) | PermissionRequested is raised when content in an iframe or any of its descendant iframes requests permission to access some privileged resources.
[WebMessageReceived](#webmessagereceived) | WebMessageReceived is raised when the [CoreWebView2Settings.IsWebMessageEnabled](corewebview2settings.md#iswebmessageenabled) setting is set and the iframe runs `window.chrome.webview.postMessage`.

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



### PostWebMessageAsJson

> void PostWebMessageAsJson(string webMessageAsJson)

Posts the specified `webMessageAsJson` to the current frame.
The event args is an instance of `MessageEvent`. The [CoreWebView2Settings.IsWebMessageEnabled](corewebview2settings.md#iswebmessageenabled) setting must be `true` or this method will fail with E_INVALIDARG. The event arg's `data` property of the event arg is the `webMessageAsJson` string parameter parsed as a JSON string into a JavaScript object. The event arg's `source` property of the event arg is a reference to the `window.chrome.webview` object. For information about sending messages from the iframe to the host, navigate to [CoreWebView2Frame.WebMessageReceived](corewebview2frame.md#webmessagereceived). The message is sent asynchronously. If a navigation occurs before the message is posted to the iframe, the message is not be sent.
Runs the message event of the `window.chrome.webview` of the iframe. JavaScript in that document may subscribe and unsubscribe to the event using the following code:
```javascript
window.chrome.webview.addEventListener('message', handler)
window.chrome.webview.removeEventListener('message', handler)
```



### PostWebMessageAsString

> void PostWebMessageAsString(string webMessageAsString)

Posts a message that is a simple string rather than a JSON string representation of a JavaScript object.
This behaves in exactly the same manner as [CoreWebView2Frame.PostWebMessageAsJson](corewebview2frame.md#postwebmessageasjson), but the `data` property of the event arg of the `window.chrome.webview` message is a string with the same value as `webMessageAsString`. Use this instead of [CoreWebView2Frame.PostWebMessageAsJson](corewebview2frame.md#postwebmessageasjson) if you want to communicate using simple strings rather than JSON objects.



### RemoveHostObjectFromScript

> void RemoveHostObjectFromScript(string name)

Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the iframe.
While new access attempts are denied, if the object is already obtained by JavaScript code in the iframe, the JavaScript code continues to have access to that object. Calling this method for a name that is already removed or was never added fails. If the iframe is destroyed this method will return fail also.




## Events

### ContentLoading

ContentLoading is raised before any content is loaded, including scripts added with [CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync](corewebview2.md#addscripttoexecuteondocumentcreatedasync). ContentLoading is not raised if a same page navigation occurs.
This operation follows the [CoreWebView2Frame.NavigationStarting](corewebview2frame.md#navigationstarting) event and precedes the [CoreWebView2Frame.DOMContentLoaded](corewebview2frame.md#domcontentloaded) and [CoreWebView2Frame.NavigationCompleted](corewebview2frame.md#navigationcompleted) events.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2Frame, [CoreWebView2ContentLoadingEventArgs](corewebview2contentloadingeventargs.md)&gt;

### DOMContentLoaded

DOMContentLoaded is raised when the initial HTML document has been parsed.
This aligns with the the document's `DOMContentLoaded` event in HTML.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2Frame, [CoreWebView2DOMContentLoadedEventArgs](corewebview2domcontentloadedeventargs.md)&gt;

### Destroyed

Destroyed event is raised when the iframe corresponding to this CoreWebView2Frame object is removed or the document containing that iframe is destroyed.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2Frame, Object&gt;

### NameChanged

NameChanged is raised when the iframe changes its `window.name` property.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2Frame, Object&gt;

### NavigationCompleted

NavigationCompleted is raised when the current frame has completely loaded (`body.onload` has been raised) or loading stopped with error.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2Frame, [CoreWebView2NavigationCompletedEventArgs](corewebview2navigationcompletedeventargs.md)&gt;

### NavigationStarting

NavigationStarting is raised when the current frame is requesting permission to navigate to a different URI.
A frame navigation will raise a [CoreWebView2Frame.NavigationStarting](corewebview2frame.md#navigationstarting) event and a [CoreWebView2.FrameNavigationStarting](corewebview2.md#framenavigationstarting) event. All of the [CoreWebView2.FrameNavigationStarting](corewebview2.md#framenavigationstarting) event handlers will be run before the [CoreWebView2Frame.NavigationStarting](corewebview2frame.md#navigationstarting) event handlers. All of the event handlers share a common [CoreWebView2NavigationStartingEventArgs](corewebview2navigationstartingeventargs.md) object. Whichever event handler is last to change the [CoreWebView2NavigationStartingEventArgs.Cancel](corewebview2navigationstartingeventargs.md#cancel) property will decide if the frame navigation will be cancelled.
Redirects raise this event as well, and the navigation id is the same as the original one. You may block corresponding navigations until the event handler returns.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2Frame, [CoreWebView2NavigationStartingEventArgs](corewebview2navigationstartingeventargs.md)&gt;

### PermissionRequested

PermissionRequested is raised when content in an iframe or any of its descendant iframes requests permission to access some privileged resources.
This relates to the `PermissionRequested` event on the `CoreWebView2`.
Both these events will be raised in the case of an iframe requesting permission. The `CoreWebView2Frame`'s event handlers will be invoked before the event handlers on the `CoreWebView2`. If the `Handled` property of the `PermissionRequestedEventArgs` is set to TRUE within the `CoreWebView2Frame` event handler, then the event will not be raised on the `CoreWebView2`, and it's event handlers will not be invoked.
In the case of nested iframes, the `PermissionRequested` event will be raised from the top level iframe.
If a deferral is not taken on the event args, the subsequent scripts are blocked until the event handler returns. If a deferral is taken, the scripts are blocked until the deferral is completed.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2Frame, [CoreWebView2PermissionRequestedEventArgs](corewebview2permissionrequestedeventargs.md)&gt;

### WebMessageReceived

WebMessageReceived is raised when the [CoreWebView2Settings.IsWebMessageEnabled](corewebview2settings.md#iswebmessageenabled) setting is set and the iframe runs `window.chrome.webview.postMessage`.
The `postMessage` function is `void postMessage(object)` where object is any object supported by JSON conversion.
When `postMessage` is called, the handler's Invoke method will be called with the `object` parameter `postMessage` converted to a JSON string.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2Frame, [CoreWebView2WebMessageReceivedEventArgs](corewebview2webmessagereceivedeventargs.md)&gt;



## Referenced by

- [CoreWebView2FrameCreatedEventArgs](corewebview2framecreatedeventargs.md)
