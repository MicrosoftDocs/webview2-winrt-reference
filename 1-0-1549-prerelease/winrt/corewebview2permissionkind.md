---
description: Indicates the kind of a permission request.
title: CoreWebView2PermissionKind
ms.date: 12/13/2022
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2PermissionKind
---

# CoreWebView2PermissionKind Enum

Indicates the kind of a permission request.

| Name |  Value | Description |
|--|--|--|
|`UnknownPermission` | 0x0  |  Indicates an unknown permission.|
|`Microphone` | 0x1  |  Indicates permission to capture audio.|
|`Camera` | 0x2  |  Indicates permission to capture video.|
|`Geolocation` | 0x3  |  Indicates permission to access geolocation.|
|`Notifications` | 0x4  |  Indicates permission to send web notifications. Apps that would like to show notifications should handle [CoreWebView2.PermissionRequested](corewebview2.md#permissionrequested) and/or [CoreWebView2Frame.PermissionRequested](corewebview2frame.md#permissionrequested) events and no browser permission prompt will be shown for notification requests. Note that push notifications are currently unavailable in WebView2.|
|`OtherSensors` | 0x5  |  Indicates permission to access generic sensor. Generic Sensor covers ambient-light-sensor, accelerometer, gyroscope, and magnetometer.|
|`ClipboardRead` | 0x6  |  Indicates permission to read the system clipboard without a user gesture.|


## Referenced by

- [CoreWebView2PermissionRequestedEventArgs](corewebview2permissionrequestedeventargs.md)
