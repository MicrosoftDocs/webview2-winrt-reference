---
description: Event args for the CoreWebView2Controller.MoveFocusRequested event.
title: CoreWebView2MoveFocusRequestedEventArgs
ms.date: 08/21/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2MoveFocusRequestedEventArgs
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- Microsoft.Web.WebView2.Core.CoreWebView2MoveFocusRequestedEventArgs
- Microsoft.Web.WebView2.Core.CoreWebView2MoveFocusRequestedEventArgs.Handled
- Microsoft.Web.WebView2.Core.CoreWebView2MoveFocusRequestedEventArgs.Reason
- Microsoft.Web.WebView2.Core.CoreWebView2MoveFocusRequestedEventArgs.get_Handled
- Microsoft.Web.WebView2.Core.CoreWebView2MoveFocusRequestedEventArgs.get_Reason
- Microsoft.Web.WebView2.Core.CoreWebView2MoveFocusRequestedEventArgs.put_Handled
---

# CoreWebView2MoveFocusRequestedEventArgs Class



Event args for the [CoreWebView2Controller.MoveFocusRequested](corewebview2controller.md#movefocusrequested) event.

## Summary

Members|Description
--|--
[Handled](#handled) | Indicates whether the event has been handled by the app.
[Reason](#reason) | Gets the reason for WebView to raise the [CoreWebView2Controller.MoveFocusRequested](corewebview2controller.md#movefocusrequested) event.

## Properties

### Handled

>  bool Handled

Indicates whether the event has been handled by the app.
If the app has moved the focus to another desired location, it should set Handled property to `true`. When `Handled` property is `false` after the event handler returns, default action is taken. The default action is to try to find the next tab stop child window in the app and try to move focus to that window. If no other window exists to move focus, focus is cycled within the web content of the WebView.

### Reason

> readonly  [CoreWebView2MoveFocusReason](corewebview2movefocusreason.md) Reason

Gets the reason for WebView to raise the [CoreWebView2Controller.MoveFocusRequested](corewebview2controller.md#movefocusrequested) event.






## Referenced by

- [CoreWebView2Controller](corewebview2controller.md)