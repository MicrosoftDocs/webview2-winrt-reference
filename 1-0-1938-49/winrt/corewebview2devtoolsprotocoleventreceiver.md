---
description: A Receiver is created for a particular DevTools Protocol event and allows you to subscribe and unsubscribe from that event.
title: CoreWebView2DevToolsProtocolEventReceiver
ms.date: 08/21/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2DevToolsProtocolEventReceiver
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- Microsoft.Web.WebView2.Core.CoreWebView2DevToolsProtocolEventReceiver
- Microsoft.Web.WebView2.Core.CoreWebView2DevToolsProtocolEventReceiver.add_DevToolsProtocolEventReceived
- Microsoft.Web.WebView2.Core.CoreWebView2DevToolsProtocolEventReceiver.remove_DevToolsProtocolEventReceived
- Microsoft.Web.WebView2.Core.CoreWebView2DevToolsProtocolEventReceiver.DevToolsProtocolEventReceived
---

# CoreWebView2DevToolsProtocolEventReceiver Class



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
