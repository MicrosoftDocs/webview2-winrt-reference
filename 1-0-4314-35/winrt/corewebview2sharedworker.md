---
description: Represents a shared worker in WebView2 and provides methods and properties for interacting with it, such as listening to destroying events, getting the script URI, origin, and top-level origin of the worker, etc.
title: CoreWebView2SharedWorker
ms.date: 10-29-2026
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2SharedWorker
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2SharedWorker
- CoreWebView2SharedWorker.Origin
- CoreWebView2SharedWorker.ScriptUri
- CoreWebView2SharedWorker.TopLevelOrigin
- CoreWebView2SharedWorker.Destroying
---

# CoreWebView2SharedWorker Class



Represents a shared worker in WebView2 and provides methods and properties for interacting with it, such as listening to destroying events, getting the script URI, origin, and top-level origin of the worker, etc.

## Summary

Members|Description
--|--
[Origin](#origin) | A string representing the URI of the origin where the worker is executing.
[ScriptUri](#scripturi) | A string representing the Uri of the script that the worker is executing.
[TopLevelOrigin](#toplevelorigin) | A string representing the URI of the top-level document that the worker is associated with.
[Destroying](#destroying) | Raised when the worker object is being destroyed.

## Properties

### Origin

> readonly  string Origin

A string representing the URI of the origin where the worker is executing.

If a worker is created with `ScriptUri` set to https://example.com/worker.js, the origin will be https://example.com/.

Refer to the Host Name Canonicalization for details on how normalization is performed.

### ScriptUri

> readonly  string ScriptUri

A string representing the Uri of the script that the worker is executing.

The `scriptUri` is a fully qualified URI, including the scheme, host, and path.
In contrast, the script URL passed to the `SharedWorker` constructor in the DOM can be relative. For more details on DOM API, see the [DOM API documentation](https://developer.mozilla.org/docs/Web/API/SharedWorker/SharedWorker).

Refer to the Host Name Canonicalization for details on how normalization is performed.
The same process applies to the script URL when a worker is created from DOM API.
The `scriptUri` property reflects this normalization, ensuring that the URL is standardized. For example, `HTTPS://EXAMPLE.COM/worker.js` is canonicalized to `https://example.com/worker.js`; `https://bücher.de/worker.js` is canonicalized to `https://xn--bcher-kva.de/worker.js`.

### TopLevelOrigin

> readonly  string TopLevelOrigin

A string representing the URI of the top-level document that the worker is associated with.

If a worker is created with `ScriptUri` set to https://example.com/worker.js, the top-level origin is https://example.com/. If the same worker is created from an iframe at https://example.com/ which is hosted on https://example2.com/, the top-level origin is https://example2.com/.

Refer to the Host Name Canonicalization section for details on how normalization is performed.

When CustomDataPartitionId is set, the `TopLevelOrigin` will be a generated site like `<guid>.invalid`. For example, if the top-level document is https://example.com/worker.js, the top-level origin will be `https://<guid>.invalid/`.




## Events

### Destroying

Raised when the worker object is being destroyed.

A worker object is being destroyed when the worker script is terminated or when the CoreWebView2SharedWorker object is being destroyed.

If the worker has already been destroyed before the event handler is registered, the handler will never be called.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2SharedWorker, Object&gt;



## Referenced by

- [CoreWebView2SharedWorkerCreatedEventArgs](corewebview2sharedworkercreatedeventargs.md)
