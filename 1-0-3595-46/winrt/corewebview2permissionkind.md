---
description: Indicates the kind of a permission request.
title: CoreWebView2PermissionKind
ms.date: 10/27/2025
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2PermissionKind
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2PermissionKind
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
|`MultipleAutomaticDownloads` | 0x7  |  Indicates permission to automatically download multiple files. Permission is requested when multiple downloads are triggered in quick succession.|
|`FileReadWrite` | 0x8  |  Indicates permission to read and write to files or folders on the device. Permission is requested when developers use the [File System Access API](https://developer.mozilla.org/docs/Web/API/File_System_Access_API) to show the file or folder picker to the end user, and then request "readwrite" permission for the user's selection.|
|`Autoplay` | 0x9  |  Indicates permission to play audio and video automatically on sites. This permission affects the autoplay attribute and play method of the audio and video HTML elements, and the start method of the Web Audio API. See the [Autoplay guide for media and Web Audio APIs](https://developer.mozilla.org/docs/Web/Media/Autoplay_guide) for details.|
|`LocalFonts` | 0xa  |  Indicates permission to use fonts on the device. Permission is requested when developers use the [Local Font Access API](https://wicg.github.io/local-font-access/) to query the system fonts available for styling web content.|
|`MidiSystemExclusiveMessages` | 0xb  |  Indicates permission to send and receive system exclusive messages to/from MIDI (Musical Instrument Digital Interface) devices. Permission is requested when developers use the [Web MIDI API](https://developer.mozilla.org/docs/Web/API/Web_MIDI_API) to request access to system exclusive MIDI messages.|
|`WindowManagement` | 0xc  |  Indicates permission to open and place windows on the screen. Permission is requested when developers use the [Multi-Screen Window Placement API](https://www.w3.org/TR/window-placement/) to get screen details.|


## Referenced by

- [CoreWebView2PermissionRequestedEventArgs](corewebview2permissionrequestedeventargs.md)
- [CoreWebView2PermissionSetting](corewebview2permissionsetting.md)
- [CoreWebView2Profile](corewebview2profile.md)
