---
description: Event args for the CoreWebView2DevToolsProtocolEventReceiver.DevToolsProtocolEventReceived event.
title: CoreWebView2DevToolsProtocolEventReceivedEventArgs
ms.date: 09/06/2022
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2DevToolsProtocolEventReceivedEventArgs
---

# CoreWebView2DevToolsProtocolEventReceivedEventArgs Class



Event args for the [CoreWebView2DevToolsProtocolEventReceiver.DevToolsProtocolEventReceived](corewebview2devtoolsprotocoleventreceiver.md#devtoolsprotocoleventreceived) event.

## Summary

Members|Description
--|--
[ParameterObjectAsJson](#parameterobjectasjson) | Gets the parameter object of the corresponding DevToolsProtocol event represented as a JSON string.
[SessionId](#sessionid) | Gets the sessionId of the target where the event originates from. Empty string is returned as sessionId if the event comes from the default session for the top page.

## Properties

### ParameterObjectAsJson

> readonly  string ParameterObjectAsJson

Gets the parameter object of the corresponding DevToolsProtocol event represented as a JSON string.

### SessionId

> readonly  string SessionId

Gets the sessionId of the target where the event originates from. Empty string is returned as sessionId if the event comes from the default session for the top page.






## Referenced by

- [CoreWebView2DevToolsProtocolEventReceiver](corewebview2devtoolsprotocoleventreceiver.md)
