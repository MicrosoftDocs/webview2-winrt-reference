---
description: Represents a dedicated worker in WebView2 and provides methods and properties for interacting with it, such as getting the script URI, posting messages, managing events related to the creation of child workers, termination, etc.
title: CoreWebView2DedicatedWorker
ms.date: 10-29-2026
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2DedicatedWorker
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2DedicatedWorker
- CoreWebView2DedicatedWorker.ScriptUri
- CoreWebView2DedicatedWorker.PostWebMessageAsJson
- CoreWebView2DedicatedWorker.PostWebMessageAsString
- CoreWebView2DedicatedWorker.DedicatedWorkerCreated
- CoreWebView2DedicatedWorker.Destroying
- CoreWebView2DedicatedWorker.WebMessageReceived
---

# CoreWebView2DedicatedWorker Class



Represents a dedicated worker in WebView2 and provides methods and properties for interacting with it, such as getting the script URI, posting messages, managing events related to the creation of child workers, termination, etc.

## Summary

Members|Description
--|--
[ScriptUri](#scripturi) | A string representing the Uri of the script that the worker is executing.
[PostWebMessageAsJson](#postwebmessageasjson) | Posts the specified `webMessageAsJson` to this worker.
[PostWebMessageAsString](#postwebmessageasstring) | Posts a message that is a simple string rather than a JSON string representation of a JavaScript object.
[DedicatedWorkerCreated](#dedicatedworkercreated) | Subscribe to this event that gets raised when a new dedicated worker is created from a dedicated worker.
[Destroying](#destroying) | Raised when the worker object is being destroyed.
[WebMessageReceived](#webmessagereceived) | `WebMessageReceived` is fired when the [CoreWebView2Settings.IsWebMessageEnabled](corewebview2settings.md#iswebmessageenabled) setting is set to `true` and the worker runs `self.chrome.webview.postMessage`.

## Properties

### ScriptUri

> readonly  string ScriptUri

A string representing the Uri of the script that the worker is executing.

The `scriptUri` is a fully qualified URI, including the scheme, host, and path.
In contrast, the script URL passed to the `Worker` constructor in the DOM can be relative. For more details on DOM API, see the [DOM API documentation](https://developer.mozilla.org/docs/Web/API/Worker/Worker).

Refer to the Host Name Canonicalization for details on how normalization is performed.
The same process applies to the script URL when a worker is created from DOM API.
The `scriptUri` property reflects this normalization, ensuring that the URL is standardized. For example, `HTTPS://EXAMPLE.COM/worker.js` is canonicalized to `https://example.com/worker.js`; `https://bücher.de/worker.js` is canonicalized to `https://xn--bcher-kva.de/worker.js`.



## Methods

### PostWebMessageAsJson

> void PostWebMessageAsJson(string webMessageAsJson)

Posts the specified `webMessageAsJson` to this worker.

The event args is an instance of `MessageEvent`. The [CoreWebView2Settings.IsWebMessageEnabled](corewebview2settings.md#iswebmessageenabled) setting must be `true` or the message will not be sent. The `data` property of the event arg is the `webMessageAsJson` string parameter parsed as a JSON string into a JavaScript object. The `source` property of the event arg is a reference to the `self.chrome.webview` object. For information about sending messages from the worker to the host, navigate to [CoreWebView2DedicatedWorker.WebMessageReceived](corewebview2dedicatedworker.md#webmessagereceived). The message is sent asynchronously. If the worker is terminated or destroyed before the message is posted, the message is discarded.

Runs the message event of the `self.chrome.webview` of this worker. Worker Javascript may subscribe and unsubscribe to the event using the following code:
```javascript
self.chrome.webview.addEventListener('message', handler)
self.chrome.webview.removeEventListener('message', handler)
```



### PostWebMessageAsString

> void PostWebMessageAsString(string webMessageAsString)

Posts a message that is a simple string rather than a JSON string representation of a JavaScript object.
This behaves in exactly the same manner as [CoreWebView2DedicatedWorker.PostWebMessageAsJson](corewebview2dedicatedworker.md#postwebmessageasjson), but the `data` property of the event arg of the `self.chrome.webview` message is a string with the same value as `webMessageAsString`. Use this instead of [CoreWebView2DedicatedWorker.PostWebMessageAsJson](corewebview2dedicatedworker.md#postwebmessageasjson) if you want to communicate using simple strings rather than JSON objects.




## Events

### DedicatedWorkerCreated

Subscribe to this event that gets raised when a new dedicated worker is created from a dedicated worker.

A Dedicated Worker is a type of web worker that allows you to run Javascript code in the background without blocking the main thread, making them useful for tasks like heavy computations, data processing, and parallel execution. It is "dedicated" because it is linked to a single parent document and cannot be shared with other scripts.

This event is raised when a dedicated worker creates a dedicated worker using the `new Worker("/worker.js")` method. See the [Worker](https://developer.mozilla.org/docs/Web/API/Worker/Worker) for more information.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2DedicatedWorker, [CoreWebView2DedicatedWorkerCreatedEventArgs](corewebview2dedicatedworkercreatedeventargs.md)&gt;

### Destroying

Raised when the worker object is being destroyed.

A worker object is being destroyed when the worker script is terminated or when the CoreWebView2DedicatedWorker object is being destroyed.

If the worker has already been destroyed before the event handler is registered, the handler will never be called.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2DedicatedWorker, Object&gt;

### WebMessageReceived

`WebMessageReceived` is fired when the [CoreWebView2Settings.IsWebMessageEnabled](corewebview2settings.md#iswebmessageenabled) setting is set to `true` and the worker runs `self.chrome.webview.postMessage`.
The `postMessage` function is `void postMessage(object)` where object is any object supported by JSON conversion.

If the worker calls `postMessage` multiple times, the corresponding `WebMessageReceived` events are guaranteed to be fired in the same order.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2DedicatedWorker, [CoreWebView2WebMessageReceivedEventArgs](corewebview2webmessagereceivedeventargs.md)&gt;



## Referenced by

- [CoreWebView2DedicatedWorkerCreatedEventArgs](corewebview2dedicatedworkercreatedeventargs.md)
