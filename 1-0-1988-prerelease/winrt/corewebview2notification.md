---
description: An object that represents a HTML Notification object.
title: CoreWebView2Notification
ms.date: 07/24/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2Notification
---

# CoreWebView2Notification Class

An object that represents a [HTML Notification object](https://developer.mozilla.org/en-US/docs/Web/API/Notification).

## Summary

Members|Description
--|--
[BadgeUri](#badgeuri) | A string containing the URI of the image used to represent the notification when there isn't enough space to display the notification itself.
[Body](#body) | A string representing the body text of the notification.
[BodyImageUri](#bodyimageuri) | A string containing the URI of an image to be displayed in the notification.
[Direction](#direction) | The text direction in which to display the notification.
[IconUri](#iconuri) | A string containing the URI of an icon to be displayed in the notification.
[IsSilent](#issilent) | Indicates whether the notification should be silent -- i.e., no sounds or vibrations should be issued, regardless of the device settings.
[Language](#language) | The notification's language, as intended to be specified using a string representing a language tag (such as `en-US`) according to [BCP47](https://datatracker.ietf.org/doc/html/rfc5646).
[RequiresInteraction](#requiresinteraction) | A boolean value indicating that a notification should remain active until the user clicks or dismisses it, rather than closing automatically.
[ShouldRenotify](#shouldrenotify) | Indicates whether the user should be notified after a new notification replaces an old one.
[Tag](#tag) | A string representing an identifying tag for the notification.
[Timestamp](#timestamp) | 
[Title](#title) | The title of the notification.
[ReportClicked](#reportclicked) | The host may run this to report the notification has been clicked, and it will cause the [click](https://developer.mozilla.org/docs/Web/API/Notification/click_event) event to be raised for non-persistent notifications.
[ReportClosed](#reportclosed) | The host may run this to report the notification was dismissed, and it will cause the [close](https://developer.mozilla.org/docs/Web/API/Notification/close_event) event to be raised for non-persistent notifications.
[ReportShown](#reportshown) | The host may run this to report the notification has been displayed and it will cause the [show](https://developer.mozilla.org/docs/Web/API/Notification/show_event) event to be raised for non-persistent notifications.
[CloseRequested](#closerequested) | This event is raised when the notification is closed by the web code, such as through `notification.close()`.

## Properties

### BadgeUri

> readonly  string BadgeUri

A string containing the URI of the image used to represent the notification when there isn't enough space to display the notification itself.
The default value is an empty string.

### Body

> readonly  string Body

A string representing the body text of the notification.
The default value is an empty string.

### BodyImageUri

> readonly  string BodyImageUri

A string containing the URI of an image to be displayed in the notification.
The default value is an empty string.

### Direction

> readonly  [CoreWebView2TextDirectionKind](corewebview2textdirectionkind.md) Direction

The text direction in which to display the notification.
This corresponds to [Notification.dir](https://developer.mozilla.org/docs/Web/API/Notification/dir) DOM API. The default value is [CoreWebView2TextDirectionKind](corewebview2textdirectionkind.md).Default.

### IconUri

> readonly  string IconUri

A string containing the URI of an icon to be displayed in the notification.
The default value is an empty string.

### IsSilent

> readonly  bool IsSilent

Indicates whether the notification should be silent -- i.e., no sounds or vibrations should be issued, regardless of the device settings.
This corresponds to [Notification.silent](https://developer.mozilla.org/docs/Web/API/Notification/silent) DOM API. The default value is `false`.

### Language

> readonly  string Language

The notification's language, as intended to be specified using a string representing a language tag (such as `en-US`) according to [BCP47](https://datatracker.ietf.org/doc/html/rfc5646).
Note that no validation is performed on this property and it can be any string the notification sender specifies. This corresponds to [Notification.lang](https://developer.mozilla.org/docs/Web/API/Notification/lang) DOM API. The default value is an empty string.

### RequiresInteraction

> readonly  bool RequiresInteraction

A boolean value indicating that a notification should remain active until the user clicks or dismisses it, rather than closing automatically.
This corresponds to [Notification.requireInteraction](https://developer.mozilla.org/docs/Web/API/Notification/requireInteraction) DOM API. Note that you may not be able to necessarily implement this due to native API limitations. The default value is `false`.

### ShouldRenotify

> readonly  bool ShouldRenotify

Indicates whether the user should be notified after a new notification replaces an old one.
This corresponds to [Notification.renotify](https://developer.mozilla.org/docs/Web/API/Notification/renotify) DOM API. The default value is `false`.

### Tag

> readonly  string Tag

A string representing an identifying tag for the notification.
This corresponds to [Notification.tag](https://developer.mozilla.org/docs/Web/API/Notification/tag) DOM API. The default value is an empty string.

### Timestamp

> readonly  double Timestamp

### Title

> readonly  string Title

The title of the notification.



## Methods

### ReportClicked

> void ReportClicked()

The host may run this to report the notification has been clicked, and it will cause the [click](https://developer.mozilla.org/docs/Web/API/Notification/click_event) event to be raised for non-persistent notifications.
You must not run this unless you are handling the [CoreWebView2.NotificationReceived](corewebview2.md#notificationreceived). API throws COMException with error code of `HRESULT_FROM_WIN32(ERROR_INVALID_STATE)` if [CoreWebView2NotificationReceivedEventArgs.Handled](corewebview2notificationreceivedeventargs.md#handled) is `false` or [CoreWebView2Notification.ReportShown](corewebview2notification.md#reportshown) has not been run when this is called.



### ReportClosed

> void ReportClosed()

The host may run this to report the notification was dismissed, and it will cause the [close](https://developer.mozilla.org/docs/Web/API/Notification/close_event) event to be raised for non-persistent notifications.
You must not run this unless you are handling the [CoreWebView2.NotificationReceived](corewebview2.md#notificationreceived). API throws COMException with error code of `HRESULT_FROM_WIN32(ERROR_INVALID_STATE)` if [CoreWebView2NotificationReceivedEventArgs.Handled](corewebview2notificationreceivedeventargs.md#handled) is `false` or [CoreWebView2Notification.ReportShown](corewebview2notification.md#reportshown) has not been run when this is called.



### ReportShown

> void ReportShown()

The host may run this to report the notification has been displayed and it will cause the [show](https://developer.mozilla.org/docs/Web/API/Notification/show_event) event to be raised for non-persistent notifications.
You must not run this unless you are handling the [CoreWebView2.NotificationReceived](corewebview2.md#notificationreceived). API throws COMException with error code of `HRESULT_FROM_WIN32(ERROR_INVALID_STATE)` if [CoreWebView2NotificationReceivedEventArgs.Handled](corewebview2notificationreceivedeventargs.md#handled) is `false` when this is called.




## Events

### CloseRequested

This event is raised when the notification is closed by the web code, such as through `notification.close()`.
You don't need to call [CoreWebView2Notification.ReportClosed](corewebview2notification.md#reportclosed) since this is coming from the web code.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2Notification, Object&gt;



## Referenced by

- [CoreWebView2NotificationReceivedEventArgs](corewebview2notificationreceivedeventargs.md)
