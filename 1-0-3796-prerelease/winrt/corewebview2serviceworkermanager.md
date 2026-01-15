---
description: This interface manages registrations for service workers in WebView2.
title: CoreWebView2ServiceWorkerManager
ms.date: 01/13/2026
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ServiceWorkerManager
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2ServiceWorkerManager
- CoreWebView2ServiceWorkerManager.GetServiceWorkerRegistrationsAsync
- CoreWebView2ServiceWorkerManager.GetServiceWorkerRegistrationsAsync
- CoreWebView2ServiceWorkerManager.ServiceWorkerRegistered
---

# CoreWebView2ServiceWorkerManager Class



This interface manages registrations for service workers in WebView2.


## Summary

Members|Description
--|--
[GetServiceWorkerRegistrationsForScope](#getserviceworkerregistrationsforscope) | Gets the service worker registrations associated with the specified scope.
[GetServiceWorkerRegistrationsAsync](#getserviceworkerregistrationsasync) | Gets a list of the service worker registrations under the same profile. 
[ServiceWorkerRegistered](#serviceworkerregistered) | A ServiceWorker is a specific type of worker that takes a JavaScript file that can control the web-page/site that it is associated with intercepting and modifying navigation and resource requests, and caching resources in a very granular fashion to give you complete control over how app behaves in certain situations.



## Methods

### GetServiceWorkerRegistrationsForScope

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;[`IVectorView`](/uwp/api/Windows.Foundation.Collections.IVectorView-1)&lt;[CoreWebView2ServiceWorkerRegistration](corewebview2serviceworkerregistration.md)&gt;&gt; GetServiceWorkerRegistrationsForScope(string scope)

Gets the service worker registrations associated with the specified scope.



### GetServiceWorkerRegistrationsAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;[`IVectorView`](/uwp/api/Windows.Foundation.Collections.IVectorView-1)&lt;[CoreWebView2ServiceWorkerRegistration](corewebview2serviceworkerregistration.md)&gt;&gt; GetServiceWorkerRegistrationsAsync()

Gets a list of the service worker registrations under the same profile.




## Events

### ServiceWorkerRegistered

A ServiceWorker is a specific type of worker that takes a JavaScript file that can control the web-page/site that it is associated with intercepting and modifying navigation and resource requests, and caching resources in a very granular fashion to give you complete control over how app behaves in certain situations.

Service workers essentially act as proxy servers that sit between web applications, the browser, and the network (when available). They run in a different context from the web page, which means they have no direct access to the DOM. Unlike dedicated and shared workers, which may have direct access to a global scope shared with other scripts, service workers operate in isolation from the DOM, ensuring a more secure and controlled environment.

This event is raised when a web application registers a service worker using the `navigator.serviceWorker.register("/sw.js")` method. See the [Service Worker Registration](https://developer.mozilla.org/docs/Web/API/ServiceWorkerRegistration) for more information.


Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2ServiceWorkerManager, [CoreWebView2ServiceWorkerRegisteredEventArgs](corewebview2serviceworkerregisteredeventargs.md)&gt;



## Referenced by

- [CoreWebView2Profile](corewebview2profile.md)
