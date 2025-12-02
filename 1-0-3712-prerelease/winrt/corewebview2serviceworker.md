---
description: This interface represents a service worker in WebView2 and provides methods and properties for interacting with it, such as getting the script uri, posting messages to it etc.
title: CoreWebView2ServiceWorker
ms.date: 12/02/2025
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ServiceWorker
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2ServiceWorker
- CoreWebView2ServiceWorker.ScriptUri
- CoreWebView2ServiceWorker.PostWebMessageAsJson
- CoreWebView2ServiceWorker.PostWebMessageAsString
- CoreWebView2ServiceWorker.Destroying
- CoreWebView2ServiceWorker.WebMessageReceived
---

# CoreWebView2ServiceWorker Class



This interface represents a service worker in WebView2 and provides methods and properties for interacting with it, such as getting the script uri, posting messages to it etc.


## Summary

Members|Description
--|--
[ScriptUri](#scripturi) | A string representing the Uri of the script that the worker is executing.
[PostWebMessageAsJson](#postwebmessageasjson) | Posts the specified `webMessageAsJson` to this worker.
[PostWebMessageAsString](#postwebmessageasstring) | Posts a message that is a simple string rather than a JSON string representation of a JavaScript object.
[Destroying](#destroying) | Add an event handler for the `CoreWebView2ServiceWorker.Destroying` event that is raised when the worker object is Destroying. A worker object is Destroying when the worker script is terminated or when the `CoreWebView2ServiceWorker` object is Destroying.
[WebMessageReceived](#webmessagereceived) | 

## Properties

### ScriptUri

> readonly  string ScriptUri

A string representing the Uri of the script that the worker is executing.

The `scriptUri` is a fully qualified URI, including the scheme, host, and path. In contrast, the `scriptURL` property of the `Worker` object in the DOM returns the relative URL of the script being executed by the worker. For more details on DOM API, see the [DOM API documentation](https://developer.mozilla.org/docs/Web/API/Worker/scriptURL).

Refer to the [Host Name Canonicalization](#host-name-canonicalization) section for details on how normalization is performed. The same process applies to the `scriptURL` when a worker is registered from DOM API. The `scriptUri` property reflects this normalization, ensuring that the URL is standardized. For example, `HTTPS://EXAMPLE.COM/worker.js` is canonicalized to `https://example.com/worker.js`; `https://b????cher.de/worker.js` is canonicalized to `https://xn--bcher-kva.de/worker.js`.




## Methods

### PostWebMessageAsJson

> void PostWebMessageAsJson(string webMessageAsJson)

Posts the specified `webMessageAsJson` to this worker.
The event args is an instance of `MessageEvent`. The [CoreWebView2Settings.IsWebMessageEnabled](corewebview2settings.md#iswebmessageenabled) setting must be `true` or the message will not be sent. The event arg's `data` property of the event arg is the `webMessageAsJson` string parameter parsed as a JSON string into a JavaScript object. The event arg's `source` property of the event arg is a reference to the `self.chrome.webview` object. For information about sending messages from the worker to the host, navigate to [CoreWebView2ServiceWorker.WebMessageReceived](corewebview2serviceworker.md#webmessagereceived). The message is sent asynchronously. If the worker is terminated or destroyed before the message is posted, the message is discarded.
Runs the message event of the `self.chrome.webview` of this worker. Worker Javascript may subscribe and unsubscribe to the event using the following code:
```javascript
self.chrome.webview.addEventListener('message', handler)
self.chrome.webview.removeEventListener('message', handler)
```




### PostWebMessageAsString

> void PostWebMessageAsString(string webMessageAsString)

Posts a message that is a simple string rather than a JSON string representation of a JavaScript object.
This behaves in exactly the same manner as [CoreWebView2ServiceWorker.PostWebMessageAsJson](corewebview2serviceworker.md#postwebmessageasjson), but the `data` property of the event arg of the `self.chrome.webview` message is a string with the same value as `webMessageAsString`. Use this instead of [CoreWebView2ServiceWorker.PostWebMessageAsJson](corewebview2serviceworker.md#postwebmessageasjson) if you want to communicate using simple strings rather than JSON objects.





## Events

### Destroying

Add an event handler for the `CoreWebView2ServiceWorker.Destroying` event that is raised when the worker object is Destroying. A worker object is Destroying when the worker script is terminated or when the `CoreWebView2ServiceWorker` object is Destroying.
If the worker has already been destroyed before the event handler is registered, the handler will never be called.


Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2ServiceWorker, Object&gt;

### WebMessageReceived

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2ServiceWorker, [CoreWebView2WebMessageReceivedEventArgs](corewebview2webmessagereceivedeventargs.md)&gt;



## Referenced by

- [CoreWebView2ServiceWorkerActivatedEventArgs](corewebview2serviceworkeractivatedeventargs.md)
- [CoreWebView2ServiceWorkerRegistration](corewebview2serviceworkerregistration.md)
