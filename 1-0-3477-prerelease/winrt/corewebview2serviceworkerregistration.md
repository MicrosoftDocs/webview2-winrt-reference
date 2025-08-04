---
description: This interface represents a service worker registration in WebView2 and provides methods and properties for interacting with it, such as getting the scope uri, active service worker, listening for service worker activation, unregistering events etc.
title: CoreWebView2ServiceWorkerRegistration
ms.date: 08/04/2025
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ServiceWorkerRegistration
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2ServiceWorkerRegistration
- CoreWebView2ServiceWorkerRegistration.ActiveServiceWorker
- CoreWebView2ServiceWorkerRegistration.Origin
- CoreWebView2ServiceWorkerRegistration.ScopeUri
- CoreWebView2ServiceWorkerRegistration.TopLevelOrigin
- CoreWebView2ServiceWorkerRegistration.ServiceWorkerActivated
- CoreWebView2ServiceWorkerRegistration.Unregistering
---

# CoreWebView2ServiceWorkerRegistration Class



This interface represents a service worker registration in WebView2 and provides methods and properties for interacting with it, such as getting the scope uri, active service worker, listening for service worker activation, unregistering events etc.


## Summary

Members|Description
--|--
[ActiveServiceWorker](#activeserviceworker) | The active service worker that was created. If there is no active service worker, it returns a null pointer.
[Origin](#origin) | A string representing the URI of the origin where the worker is executing.
[ScopeUri](#scopeuri) | The `scopeUri` is a fully qualified URI, including the scheme, host and path, that specifies the range of URLs a service worker can control.
[TopLevelOrigin](#toplevelorigin) | A string representing the URI of the top-level document that the worker is associated with.
[ServiceWorkerActivated](#serviceworkeractivated) | Adds an event handler for the `ServiceWorkerActivated` event.
[Unregistering](#unregistering) | Add an event handler for the `Unregistering` event that is raised when the worker registration is unregistered using the JS api `registration.unregister()`. See the [Unregister](https://developer.mozilla.org/docs/Web/API/ServiceWorkerRegistration/unregister) for more information

## Properties

### ActiveServiceWorker

> readonly  [CoreWebView2ServiceWorker](corewebview2serviceworker.md) ActiveServiceWorker

The active service worker that was created. If there is no active service worker, it returns a null pointer.

The active service worker is the service worker that controls the pages within the scope of the registration. See the [Service Worker] (https://developer.mozilla.org/docs/Web/API/ServiceWorker) for more information.

This corresponds to the `active` property of the `ServiceWorkerRegistration` object in the DOM. For more information, see the [MDN documentation]
(https://developer.mozilla.org/docs/Web/API/ServiceWorkerRegistration/active).


### Origin

> readonly  string Origin

A string representing the URI of the origin where the worker is executing.

If a worker created with `ScriptUri` set to https://example.com/worker.js, the origin will be https://example.com/.

Refer to the [Host Name Canonicalization](#host-name-canonicalization) section for details on how normalization is performed.


### ScopeUri

> readonly  string ScopeUri

The `scopeUri` is a fully qualified URI, including the scheme, host and path, that specifies the range of URLs a service worker can control.

When registering a service worker, if no scope is specified, it defaults to the directory where the service worker script resides. For example, if the script is located at https://example.com/app/sw.js, the default `scopeUri` would be https://example.com/app/. However, if a scope is provided, it is defined relative to the application's base URI. For instance, if an application at https://example.com/ registers a service worker with a scope of /app/, the resulting `scopeUri` is https://example.com/app/.

Refer to the [Host Name Canonicalization](#host-name-canonicalization) section for details on how normalization is performed. The same process applies to the `Scope` when a service worker is registered from DOM API. The `scopeUri` property reflects this normalization, ensuring that the URI is standardized. For example, `HTTPS://EXAMPLE.COM/app/` is canonicalized to `https://example.com/app/`; `https://b????cher.de/` is canonicalized to `https://xn--bcher-kva.de/`.

The `scope` property of the `ServiceWorkerRegistration` object in the DOM returns the relative URL based on the application's base URI, while this property always returns a fully qualified URI.  For more information on DOM API, see the [MDN documentation](https://developer.mozilla.org/docs/Web/API/ServiceWorkerRegistration/scope).


### TopLevelOrigin

> readonly  string TopLevelOrigin

A string representing the URI of the top-level document that the worker is associated with.

If a worker is created with `ScriptUri` set to https://example.com/worker.js, the top-level origin is https://example.com/. If the same worker is created from a iframe at https://example.com/ which is hosted on https://example2.com/, the top-level origin is https://example2.com/.

Refer to the [Host Name Canonicalization](#host-name-canonicalization) section for details on how normalization is performed.

When CustomDataPartitionId is set, the `TopLevelOrigin` will be a generated site like &lt;guid&gt;.invalid. For example, if the top-level document is https://example.com/worker.js, the top-level origin will be `https://&lt;guid&gt;.invalid/`.






## Events

### ServiceWorkerActivated

Adds an event handler for the `ServiceWorkerActivated` event.

This event is raised when a service worker is activated. A service worker is activated when its script has been successfully registered and it is ready to control the pages within the scope of the registration.

This event is also raised when an updated version of a service worker reaches the active state. In such a case, the existing CoreWebView2ServiceWorker object is destroying, and this event is raised with a new CoreWebView2ServiceWorker object representing the updated service worker. The active service worker is the one that receives fetch and message events for the pages it controls. See the [Service Worker](https://developer.mozilla.org/en-US/docs/Web/API/ServiceWorkerRegistration/active) documentation for more information.

If you register for the `ServiceWorkerActivated` event and the registration already has an active worker, the event handler is not called immediately. Instead, it waits for the next activation event to occur. Therefore, you should first check if an active service worker is running by using the `ActiveServiceWorker` property.


Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2ServiceWorkerRegistration, [CoreWebView2ServiceWorkerActivatedEventArgs](corewebview2serviceworkeractivatedeventargs.md)&gt;

### Unregistering

Add an event handler for the `Unregistering` event that is raised when the worker registration is unregistered using the JS api `registration.unregister()`. See the [Unregister](https://developer.mozilla.org/docs/Web/API/ServiceWorkerRegistration/unregister) for more information


Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2ServiceWorkerRegistration, Object&gt;



## Referenced by

- [CoreWebView2ServiceWorkerRegisteredEventArgs](corewebview2serviceworkerregisteredeventargs.md)
