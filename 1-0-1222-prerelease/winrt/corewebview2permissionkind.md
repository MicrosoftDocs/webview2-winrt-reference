---
description: Indicates the kind of a permission request.
title: CoreWebView2PermissionKind
ms.date: 04/12/2022
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
|`Notifications` | 0x4  |  Indicates permission to send web notifications. This permission request is currently auto-rejected and no event is raised for it.|
|`OtherSensors` | 0x5  |  Indicates permission to access generic sensor. Generic Sensor covers ambient-light-sensor, accelerometer, gyroscope, and magnetometer.|
|`ClipboardRead` | 0x6  |  Indicates permission to read the system clipboard without a user gesture.|


## Referenced by

- [CoreWebView2PermissionRequestedEventArgs](corewebview2permissionrequestedeventargs.md)
