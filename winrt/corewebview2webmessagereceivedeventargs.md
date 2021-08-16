---
description: Event args for the CoreWebView2.WebMessageReceived event.
title: CoreWebView2WebMessageReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/16/2021
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2WebMessageReceivedEventArgs
---

# runtimeclass CoreWebView2WebMessageReceivedEventArgs



Event args for the [CoreWebView2.WebMessageReceived](corewebview2.md#webmessagereceived) event.

## Summary

Members|Description
--|--
[Source](#source) | Gets the URI of the document that sent this web message.
[WebMessageAsJson](#webmessageasjson) | Gets the message posted from the WebView content to the host converted to a JSON string.
[TryGetWebMessageAsString](#trygetwebmessageasstring) | Gets the message posted from the WebView content to the host as a string.

## Properties

### Source

> readonly  string Source

Gets the URI of the document that sent this web message.

### WebMessageAsJson

> readonly  string WebMessageAsJson

Gets the message posted from the WebView content to the host converted to a JSON string.

Run this operation to communicate using JavaScript objects.

For example, the following `postMessage` runs result in the following WebMessageAsJson values:

```
postMessage({'a': 'b'})      "{\\"a\\": \\"b\\"}"
postMessage(1.2)             "1.2"
postMessage('example')       "\\"example\\""
```



## Methods

### TryGetWebMessageAsString

> string TryGetWebMessageAsString()

Gets the message posted from the WebView content to the host as a string.

Run this operation to communicate using simple strings.

For example the following `postMessage` runs result in the following values returned by TryWebMessageAsString:

```
postMessage({'a': 'b'})      ArgumentException
postMessage(1.2)             ArgumentException
postMessage('example')       "example"
```






## Referenced by

- [CoreWebView2](corewebview2.md)
