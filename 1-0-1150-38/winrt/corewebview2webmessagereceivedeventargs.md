---
description: Event args for the CoreWebView2.WebMessageReceived event.
title: CoreWebView2WebMessageReceivedEventArgs
ms.date: 03/10/2022
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2WebMessageReceivedEventArgs
---

# CoreWebView2WebMessageReceivedEventArgs Class



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



## Methods

### TryGetWebMessageAsString

> string TryGetWebMessageAsString()

Gets the message posted from the WebView content to the host as a string.
Run this operation to communicate using simple strings.






## Referenced by

- [CoreWebView2](corewebview2.md)
- [CoreWebView2Frame](corewebview2frame.md)
