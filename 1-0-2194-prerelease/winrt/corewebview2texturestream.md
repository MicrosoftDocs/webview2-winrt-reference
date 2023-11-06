---
description: CoreWebView2 Texture Stream.
title: CoreWebView2TextureStream
ms.date: 11/06/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2TextureStream
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- Microsoft.Web.WebView2.Core.CoreWebView2TextureStream
- Microsoft.Web.WebView2.Core.CoreWebView2TextureStream.Id
- Microsoft.Web.WebView2.Core.CoreWebView2TextureStream.AddAllowedOrigin
- Microsoft.Web.WebView2.Core.CoreWebView2TextureStream.CloseTexture
- Microsoft.Web.WebView2.Core.CoreWebView2TextureStream.CreateTexture
- Microsoft.Web.WebView2.Core.CoreWebView2TextureStream.GetAvailableTexture
- Microsoft.Web.WebView2.Core.CoreWebView2TextureStream.PresentTexture
- Microsoft.Web.WebView2.Core.CoreWebView2TextureStream.RemoveAllowedOrigin
- Microsoft.Web.WebView2.Core.CoreWebView2TextureStream.SetD3DDevice
- Microsoft.Web.WebView2.Core.CoreWebView2TextureStream.Stop
- Microsoft.Web.WebView2.Core.CoreWebView2TextureStream.add_ErrorReceived
- Microsoft.Web.WebView2.Core.CoreWebView2TextureStream.add_StartRequested
- Microsoft.Web.WebView2.Core.CoreWebView2TextureStream.add_Stopped
- Microsoft.Web.WebView2.Core.CoreWebView2TextureStream.add_WebTextureReceived
- Microsoft.Web.WebView2.Core.CoreWebView2TextureStream.add_WebTextureStreamStopped
- Microsoft.Web.WebView2.Core.CoreWebView2TextureStream.get_Id
- Microsoft.Web.WebView2.Core.CoreWebView2TextureStream.remove_ErrorReceived
- Microsoft.Web.WebView2.Core.CoreWebView2TextureStream.remove_StartRequested
- Microsoft.Web.WebView2.Core.CoreWebView2TextureStream.remove_Stopped
- Microsoft.Web.WebView2.Core.CoreWebView2TextureStream.remove_WebTextureReceived
- Microsoft.Web.WebView2.Core.CoreWebView2TextureStream.remove_WebTextureStreamStopped
- Microsoft.Web.WebView2.Core.CoreWebView2TextureStream.ErrorReceived
- Microsoft.Web.WebView2.Core.CoreWebView2TextureStream.StartRequested
- Microsoft.Web.WebView2.Core.CoreWebView2TextureStream.Stopped
- Microsoft.Web.WebView2.Core.CoreWebView2TextureStream.WebTextureReceived
- Microsoft.Web.WebView2.Core.CoreWebView2TextureStream.WebTextureStreamStopped
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
