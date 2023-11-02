---
description: 
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

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2TextureStream, [CoreWebView2TextureStreamErrorReceivedEventArgs](corewebview2texturestreamerrorreceivedeventargs.md)&gt;

### StartRequested

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2TextureStream, Object&gt;

### Stopped

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2TextureStream, Object&gt;

### WebTextureReceived

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2TextureStream, [CoreWebView2TextureStreamWebTextureReceivedEventArgs](corewebview2texturestreamwebtexturereceivedeventargs.md)&gt;

### WebTextureStreamStopped

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2TextureStream, Object&gt;



## Referenced by

- [CoreWebView2Environment](corewebview2environment.md)
