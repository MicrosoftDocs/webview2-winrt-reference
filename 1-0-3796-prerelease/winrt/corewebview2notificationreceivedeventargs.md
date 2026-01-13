---
description: Event args for the CoreWebView2.NotificationReceived.
title: CoreWebView2NotificationReceivedEventArgs
ms.date: 01/13/2026
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2NotificationReceivedEventArgs
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2NotificationReceivedEventArgs
- CoreWebView2NotificationReceivedEventArgs.Handled
- CoreWebView2NotificationReceivedEventArgs.Notification
- CoreWebView2NotificationReceivedEventArgs.SenderOrigin
- CoreWebView2NotificationReceivedEventArgs.GetDeferral
---

# CoreWebView2NotificationReceivedEventArgs Class



Event args for the [CoreWebView2.NotificationReceived](corewebview2.md#notificationreceived).

## Summary

Members|Description
--|--
[Handled](#handled) | Sets whether the [CoreWebView2.NotificationReceived](corewebview2.md#notificationreceived) is handled by the host after the event handler completes or if there is a deferral then after the deferral is completed.
[Notification](#notification) | The notification that was received.
[SenderOrigin](#senderorigin) | The origin of the web content that sends the notification, such as `https://example.com/` or `https://www.example.com/`.
[GetDeferral](#getdeferral) | Gets a Deferral object.

## Properties

### Handled

>  bool Handled

Sets whether the [CoreWebView2.NotificationReceived](corewebview2.md#notificationreceived) is handled by the host after the event handler completes or if there is a deferral then after the deferral is completed.
If [CoreWebView2NotificationReceivedEventArgs.Handled](corewebview2notificationreceivedeventargs.md#handled) is set to `true` then WebView will not display the notification with the default UI, and the host will be responsible for handling the notification and for letting the web content know that the notification has been displayed, clicked, or closed. You must set [CoreWebView2NotificationReceivedEventArgs.Handled](corewebview2notificationreceivedeventargs.md#handled) to `true` before you call [CoreWebView2Notification.ReportShown](corewebview2notification.md#reportshown), <see cref="CoreWebView2Notification.ReportClicked()"/> and [CoreWebView2Notification.ReportClosed](corewebview2notification.md#reportclosed), otherwise they will fail with `HRESULT_FROM_WIN32(ERROR_INVALID_STATE)`. If after the event handler or deferral completes [CoreWebView2NotificationReceivedEventArgs.Handled](corewebview2notificationreceivedeventargs.md#handled) is set to `false` then WebView will display the default notification UI. Note that you cannot un-handle this event once you have set [CoreWebView2NotificationReceivedEventArgs.Handled](corewebview2notificationreceivedeventargs.md#handled) to be `true`. The initial value is `false`.

### Notification

> readonly  [CoreWebView2Notification](corewebview2notification.md) Notification

The notification that was received.
You can access the properties on the Notification object to show your own notification.

### SenderOrigin

> readonly  string SenderOrigin

The origin of the web content that sends the notification, such as `https://example.com/` or `https://www.example.com/`.



## Methods

### GetDeferral

> [Deferral](/uwp/api/Windows.Foundation.Deferral) GetDeferral()

Gets a Deferral object.
Use this to Complete the event at a later time.






## Referenced by

- [CoreWebView2](corewebview2.md)
