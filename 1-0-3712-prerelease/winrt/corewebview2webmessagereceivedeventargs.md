---
description: Event args for the CoreWebView2.WebMessageReceived event.
title: CoreWebView2WebMessageReceivedEventArgs
ms.date: 12/02/2025
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2WebMessageReceivedEventArgs
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2WebMessageReceivedEventArgs
- CoreWebView2WebMessageReceivedEventArgs.AdditionalObjects
- CoreWebView2WebMessageReceivedEventArgs.Source
- CoreWebView2WebMessageReceivedEventArgs.WebMessageAsJson
- CoreWebView2WebMessageReceivedEventArgs.TryGetWebMessageAsString
---

# CoreWebView2WebMessageReceivedEventArgs Class



Event args for the [CoreWebView2.WebMessageReceived](corewebview2.md#webmessagereceived) event.

## Summary

Members|Description
--|--
[AdditionalObjects](#additionalobjects) | Additional received WebMessage objects.
[Source](#source) | Gets the URI of the document that sent this web message.
[WebMessageAsJson](#webmessageasjson) | Gets the message posted from the WebView content to the host converted to a JSON string.
[TryGetWebMessageAsString](#trygetwebmessageasstring) | Gets the message posted from the WebView content to the host as a string.

## Properties

### AdditionalObjects

> readonly  [`IVectorView`](/uwp/api/Windows.Foundation.Collections.IVectorView-1)&lt;Object&gt; AdditionalObjects

Additional received WebMessage objects.
To pass `AdditionalObjects` via WebMessage to the app, use the `chrome.webview.postMessageWithAdditionalObjects` content API. Any DOM object type that can be natively representable that has been passed in to `additionalObjects` parameter will be accessible here. Currently a WebMessage object can be the [CoreWebView2File](corewebview2file.md) type.
Entries in the collection can be `nullptr` if `null` or `undefined` was passed. Cast the object to the native type to access its specific properties.

### Source

> readonly  string Source

Gets the URI of the document that sent this web message.

### WebMessageAsJson

> readonly  string WebMessageAsJson

Gets the message posted from the WebView content to the host converted to a JSON string.
Run this operation to communicate using JavaScript objects.



## Methods

### TryGetWebMessageAsString

> string TryGetWebMessageAsString()

Gets the message posted from the WebView content to the host as a string.
Run this operation to communicate using simple strings.






## Referenced by

- [CoreWebView2](corewebview2.md)
- [CoreWebView2DedicatedWorker](corewebview2dedicatedworker.md)
- [CoreWebView2Frame](corewebview2frame.md)
- [CoreWebView2ServiceWorker](corewebview2serviceworker.md)
