---
description: Kinds of errors that can be reported by the `ErrorReceived` event.
title: CoreWebView2TextureStreamErrorKind
ms.date: 11/11/2026
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2TextureStreamErrorKind
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2TextureStreamErrorKind
---

# CoreWebView2TextureStreamErrorKind Enum

Kinds of errors that can be reported by the `ErrorReceived` event.

| Name |  Value | Description |
|--|--|--|
|`NoVideoTrackStarted` | 0x0  |  CreateTexture/PresentTexture and so on should fail if the texture stream is in the stopped state rather than using the error event. But there can be edge cases where the browser process knows the texture stream is in the stopped state and the host app process texture stream doesn't yet know that. Like the 10 second issue or if the script side has stopped the stream.|
|`TextureError` | 0x1  |  The texture already has been removed using CloseTexture.|
|`TextureInUse` | 0x2  |  The texture to be presented is already in use for rendering. Call GetAvailableTexture to determine an available texture to present. The developer can technically call PresentTexture multiple times, but the first call make input texture "in use" until the browser renders it and returns the texture as "recycle" so that it can be a member of available textures.|


## Referenced by

- [CoreWebView2TextureStreamErrorReceivedEventArgs](corewebview2texturestreamerrorreceivedeventargs.md)
