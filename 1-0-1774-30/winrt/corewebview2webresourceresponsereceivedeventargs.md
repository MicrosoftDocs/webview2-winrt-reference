---
description: Event args for the CoreWebView2.WebResourceResponseReceived event.
title: CoreWebView2WebResourceResponseReceivedEventArgs
ms.date: 05/05/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2WebResourceResponseReceivedEventArgs
---

# CoreWebView2WebResourceResponseReceivedEventArgs Class



Event args for the [CoreWebView2.WebResourceResponseReceived](corewebview2.md#webresourceresponsereceived) event.

## Summary

Members|Description
--|--
[Request](#request) | Gets the request object for the web resource, as committed.
[Response](#response) | Gets view of the response object received for the web resource.

## Properties

### Request

> readonly  [CoreWebView2WebResourceRequest](corewebview2webresourcerequest.md) Request

Gets the request object for the web resource, as committed.
This includes headers added by the network stack that were not be included during the associated [CoreWebView2.WebResourceRequested](corewebview2.md#webresourcerequested) event, such as Authentication headers. Modifications to this object have no effect on how the request is processed as it has already been sent.

### Response

> readonly  [CoreWebView2WebResourceResponseView](corewebview2webresourceresponseview.md) Response

Gets view of the response object received for the web resource.






## Referenced by

- [CoreWebView2](corewebview2.md)