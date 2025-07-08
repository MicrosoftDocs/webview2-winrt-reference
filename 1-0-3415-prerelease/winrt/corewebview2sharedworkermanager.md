---
description: 
title: CoreWebView2SharedWorkerManager
ms.date: 07/08/2025
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2SharedWorkerManager
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2SharedWorkerManager
- CoreWebView2SharedWorkerManager.GetSharedWorkersAsync
- CoreWebView2SharedWorkerManager.SharedWorkerCreated
---

# CoreWebView2SharedWorkerManager Class



## Summary

Members|Description
--|--
[GetSharedWorkersAsync](#getsharedworkersasync) | 
[SharedWorkerCreated](#sharedworkercreated) | Add an event handler for the `SharedWorkerCreated` event.



## Methods

### GetSharedWorkersAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;[`IVectorView`](/uwp/api/Windows.Foundation.Collections.IVectorView-1)&lt;[CoreWebView2SharedWorker](corewebview2sharedworker.md)&gt;&gt; GetSharedWorkersAsync()




## Events

### SharedWorkerCreated

Add an event handler for the `SharedWorkerCreated` event.

A SharedWorker is a specific type of worker that can be accessed from several browsing contexts, such as multiple windows, iframes, or even other workers. Unlike Dedicated Workers, which have their own separate global scope, SharedWorkers share a common global scope called SharedWorkerGlobalScope.

This event is raised when a web application creates a shared worker using the `new SharedWorker("worker.js")` method. See the
[Shared Worker](https://developer.mozilla.org/docs/Web/API/SharedWorker) for more information.


Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2SharedWorkerManager, [CoreWebView2SharedWorkerCreatedEventArgs](corewebview2sharedworkercreatedeventargs.md)&gt;



## Referenced by

- [CoreWebView2Profile](corewebview2profile.md)
