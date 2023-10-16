---
description: 
title: CoreWebView2Controller
ms.date: 10/16/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2Controller
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- Microsoft.Web.WebView2.Core.CoreWebView2Controller
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.AllowExternalDrop
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.Bounds
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.BoundsMode
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.CoreWebView2
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.DefaultBackgroundColor
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.IsBrowserHitTransparent
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.IsVisible
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.ParentWindow
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.RasterizationScale
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.ShouldDetectMonitorScaleChanges
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.ZoomFactor
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.Close
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.MoveFocus
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.NotifyParentWindowPositionChanged
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.SetBoundsAndZoomFactor
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.add_AcceleratorKeyPressed
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.add_GotFocus
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.add_LostFocus
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.add_MoveFocusRequested
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.add_RasterizationScaleChanged
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.add_ZoomFactorChanged
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.get_AllowExternalDrop
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.get_Bounds
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.get_BoundsMode
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.get_CoreWebView2
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.get_DefaultBackgroundColor
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.get_IsBrowserHitTransparent
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.get_IsVisible
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.get_ParentWindow
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.get_RasterizationScale
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.get_ShouldDetectMonitorScaleChanges
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.get_ZoomFactor
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.put_AllowExternalDrop
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.put_Bounds
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.put_BoundsMode
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.put_DefaultBackgroundColor
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.put_IsVisible
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.put_ParentWindow
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.put_RasterizationScale
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.put_ShouldDetectMonitorScaleChanges
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.put_ZoomFactor
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.remove_AcceleratorKeyPressed
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.remove_GotFocus
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.remove_LostFocus
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.remove_MoveFocusRequested
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.remove_RasterizationScaleChanged
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.remove_ZoomFactorChanged
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.AcceleratorKeyPressed
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.GotFocus
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.LostFocus
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.MoveFocusRequested
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.RasterizationScaleChanged
- Microsoft.Web.WebView2.Core.CoreWebView2Controller.ZoomFactorChanged
---

# CoreWebView2Controller Class



## Summary

Members|Description
--|--
[AllowExternalDrop](#allowexternaldrop) | 
[Bounds](#bounds) | 
[BoundsMode](#boundsmode) | 
[CoreWebView2](#corewebview2) | 
[DefaultBackgroundColor](#defaultbackgroundcolor) | 
[IsBrowserHitTransparent](#isbrowserhittransparent) | 
[IsVisible](#isvisible) | 
[ParentWindow](#parentwindow) | 
[RasterizationScale](#rasterizationscale) | 
[ShouldDetectMonitorScaleChanges](#shoulddetectmonitorscalechanges) | 
[ZoomFactor](#zoomfactor) | 
[Close](#close) | 
[MoveFocus](#movefocus) | 
[NotifyParentWindowPositionChanged](#notifyparentwindowpositionchanged) | 
[SetBoundsAndZoomFactor](#setboundsandzoomfactor) | 
[AcceleratorKeyPressed](#acceleratorkeypressed) | 
[GotFocus](#gotfocus) | 
[LostFocus](#lostfocus) | 
[MoveFocusRequested](#movefocusrequested) | 
[RasterizationScaleChanged](#rasterizationscalechanged) | 
[ZoomFactorChanged](#zoomfactorchanged) | 

## Properties

### AllowExternalDrop

>  bool AllowExternalDrop

### Bounds

>  [Rect](/uwp/api/Windows.Foundation.Rect) Bounds

### BoundsMode

>  [CoreWebView2BoundsMode](corewebview2boundsmode.md) BoundsMode

### CoreWebView2

> readonly  [CoreWebView2](corewebview2.md) CoreWebView2

### DefaultBackgroundColor

>  [Color](/uwp/api/Windows.UI.Color) DefaultBackgroundColor

### IsBrowserHitTransparent

> readonly  bool IsBrowserHitTransparent

### IsVisible

>  bool IsVisible

### ParentWindow

>  [CoreWebView2ControllerWindowReference](corewebview2controllerwindowreference.md) ParentWindow

### RasterizationScale

>  double RasterizationScale

### ShouldDetectMonitorScaleChanges

>  bool ShouldDetectMonitorScaleChanges

### ZoomFactor

>  double ZoomFactor



## Methods

### Close

> void Close()



### MoveFocus

> void MoveFocus([CoreWebView2MoveFocusReason](corewebview2movefocusreason.md) reason)



### NotifyParentWindowPositionChanged

> void NotifyParentWindowPositionChanged()



### SetBoundsAndZoomFactor

> void SetBoundsAndZoomFactor([Rect](/uwp/api/Windows.Foundation.Rect) Bounds, double ZoomFactor)




## Events

### AcceleratorKeyPressed

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2Controller, [CoreWebView2AcceleratorKeyPressedEventArgs](corewebview2acceleratorkeypressedeventargs.md)&gt;

### GotFocus

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2Controller, Object&gt;

### LostFocus

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2Controller, Object&gt;

### MoveFocusRequested

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2Controller, [CoreWebView2MoveFocusRequestedEventArgs](corewebview2movefocusrequestedeventargs.md)&gt;

### RasterizationScaleChanged

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2Controller, Object&gt;

### ZoomFactorChanged

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2Controller, Object&gt;

