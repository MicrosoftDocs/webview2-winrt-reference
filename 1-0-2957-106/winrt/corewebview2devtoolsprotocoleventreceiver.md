---
title: CoreWebView2DevToolsProtocolEventReceiver
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/13/2025
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2DevToolsProtocolEventReceiver
---

# runtimeClass CoreWebView2DevToolsProtocolEventReceiver



A Receiver is created for a particular DevTools Protocol event and allows you to subscribe and unsubscribe from that event.
Obtained from the WebView object using [CoreWebView2.GetDevToolsProtocolEventReceiver](corewebview2.md#getdevtoolsprotocoleventreceiver).

## Summary

Members|Description
--|--
[DevToolsProtocolEventReceived](#devtoolsprotocoleventreceived) | DevToolsProtocolEventReceived is raised when the corresponding DevToolsProtocol event is raised.




## Events

### DevToolsProtocolEventReceived

DevToolsProtocolEventReceived is raised when the corresponding DevToolsProtocol event is raised.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2](corewebview2.md), [CoreWebView2DevToolsProtocolEventReceivedEventArgs](corewebview2devtoolsprotocoleventreceivedeventargs.md)&gt;



## Referenced by

- [CoreWebView2](corewebview2.md)
