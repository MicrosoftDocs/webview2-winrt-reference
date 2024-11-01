---
title: CoreWebView2TextureStream
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/01/2024
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2TextureStream
---

# runtimeClass CoreWebView2TextureStream



## Summary

Members|Description
--|--
[Id](#id) | 
[AddAllowedOrigin](#addallowedorigin) | 
[CloseTexture](#closetexture) | 
[CreateTexture](#createtexture) | 
[GetAvailableTexture](#getavailabletexture) | 
[PresentTexture](#presenttexture) | 
[RemoveAllowedOrigin](#removeallowedorigin) | 
[SetD3DDevice](#setd3ddevice) | 
[Stop](#stop) | 
[ErrorReceived](#errorreceived) | 
[StartRequested](#startrequested) | 
[Stopped](#stopped) | 
[WebTextureReceived](#webtexturereceived) | 
[WebTextureStreamStopped](#webtexturestreamstopped) | 

## Properties

### Id

> readonly  string Id



## Methods

### AddAllowedOrigin

> void AddAllowedOrigin(string origin, int value)



### CloseTexture

> void CloseTexture([CoreWebView2Texture](corewebview2texture.md) texture)



### CreateTexture

> [CoreWebView2Texture](corewebview2texture.md) CreateTexture(uint32_t widthInTexels, uint32_t heightInTexels)



### GetAvailableTexture

> [CoreWebView2Texture](corewebview2texture.md) GetAvailableTexture()



### PresentTexture

> void PresentTexture([CoreWebView2Texture](corewebview2texture.md) texture)



### RemoveAllowedOrigin

> void RemoveAllowedOrigin(string origin)



### SetD3DDevice

> void SetD3DDevice(Object d3dDevice)



### Stop

> void Stop()




## Events

### ErrorReceived

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2TextureStream](corewebview2texturestream.md), [CoreWebView2TextureStreamErrorReceivedEventArgs](corewebview2texturestreamerrorreceivedeventargs.md)&gt;

### StartRequested

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2TextureStream](corewebview2texturestream.md), Object&gt;

### Stopped

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2TextureStream](corewebview2texturestream.md), Object&gt;

### WebTextureReceived

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2TextureStream](corewebview2texturestream.md), [CoreWebView2TextureStreamWebTextureReceivedEventArgs](corewebview2texturestreamwebtexturereceivedeventargs.md)&gt;

### WebTextureStreamStopped

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2TextureStream](corewebview2texturestream.md), Object&gt;



## Referenced by

- [CoreWebView2Environment](corewebview2environment.md)
