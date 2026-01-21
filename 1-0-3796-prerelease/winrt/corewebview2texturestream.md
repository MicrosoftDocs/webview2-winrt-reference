---
description: CoreWebView2 Texture Stream.
title: CoreWebView2TextureStream
ms.date: 01/13/2026
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2TextureStream
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2TextureStream
- CoreWebView2TextureStream.Id
- CoreWebView2TextureStream.AddAllowedOrigin
- CoreWebView2TextureStream.CloseTexture
- CoreWebView2TextureStream.CreateTexture
- CoreWebView2TextureStream.GetAvailableTexture
- CoreWebView2TextureStream.PresentTexture
- CoreWebView2TextureStream.RemoveAllowedOrigin
- CoreWebView2TextureStream.SetD3DDevice
- CoreWebView2TextureStream.Stop
- CoreWebView2TextureStream.ErrorReceived
- CoreWebView2TextureStream.StartRequested
- CoreWebView2TextureStream.Stopped
- CoreWebView2TextureStream.WebTextureReceived
- CoreWebView2TextureStream.WebTextureStreamStopped
---

# CoreWebView2TextureStream Class



CoreWebView2 Texture Stream.

## Summary

Members|Description
--|--
[Id](#id) | Retrives texture stream id.
[AddAllowedOrigin](#addallowedorigin) | Adds allowed origin for texture stream and web texture stream.
[CloseTexture](#closetexture) | Closes created texture.
[CreateTexture](#createtexture) | Creates texture buffer that the host can write to for the browser rendering.
[GetAvailableTexture](#getavailabletexture) | Gets reusable texture.
[PresentTexture](#presenttexture) | Present texture to the browser's renderer.
[RemoveAllowedOrigin](#removeallowedorigin) | Removes allowed origin for texture stream and web texture stream.
[SetD3DDevice](#setd3ddevice) | Sets D3D device with new device.
[Stop](#stop) | Stops presenting texture stream.
[ErrorReceived](#errorreceived) | Registers texture stream error event.
[StartRequested](#startrequested) | Registers texture stream request from the Javascript.
[Stopped](#stopped) | Registers texture stream stopped event.
[WebTextureReceived](#webtexturereceived) | Registers web texture receiving event.
[WebTextureStreamStopped](#webtexturestreamstopped) | Registers web texture stopped event.

## Properties

### Id

> readonly  string Id

Retrives texture stream id.



## Methods

### AddAllowedOrigin

> void AddAllowedOrigin(string origin, int value)

Adds allowed origin for texture stream and web texture stream.



### CloseTexture

> void CloseTexture([CoreWebView2Texture](corewebview2texture.md) texture)

Closes created texture.



### CreateTexture

> [CoreWebView2Texture](corewebview2texture.md) CreateTexture(uint32_t widthInTexels, uint32_t heightInTexels)

Creates texture buffer that the host can write to for the browser rendering.



### GetAvailableTexture

> [CoreWebView2Texture](corewebview2texture.md) GetAvailableTexture()

Gets reusable texture.



### PresentTexture

> void PresentTexture([CoreWebView2Texture](corewebview2texture.md) texture)

Present texture to the browser's renderer.



### RemoveAllowedOrigin

> void RemoveAllowedOrigin(string origin)

Removes allowed origin for texture stream and web texture stream.




### SetD3DDevice

> void SetD3DDevice(Object d3dDevice)

Sets D3D device with new device.



### Stop

> void Stop()

Stops presenting texture stream.




## Events

### ErrorReceived

Registers texture stream error event.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2TextureStream, [CoreWebView2TextureStreamErrorReceivedEventArgs](corewebview2texturestreamerrorreceivedeventargs.md)&gt;

### StartRequested

Registers texture stream request from the Javascript.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2TextureStream, Object&gt;

### Stopped

Registers texture stream stopped event.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2TextureStream, Object&gt;

### WebTextureReceived

Registers web texture receiving event.


Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2TextureStream, [CoreWebView2TextureStreamWebTextureReceivedEventArgs](corewebview2texturestreamwebtexturereceivedeventargs.md)&gt;

### WebTextureStreamStopped

Registers web texture stopped event.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2TextureStream, Object&gt;



## Referenced by

- [CoreWebView2Environment](corewebview2environment.md)
