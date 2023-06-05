---
description: The owner of the CoreWebView2 object that provides support for resizing, showing and hiding, focusing, and other functionality related to windowing and composition.
title: CoreWebView2Controller
ms.date: 06/05/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2Controller
---

# CoreWebView2Controller Class



The owner of the [CoreWebView2](corewebview2.md) object that provides support for resizing, showing and hiding, focusing, and other functionality related to windowing and composition.
The CoreWebView2Controller owns the [CoreWebView2](corewebview2.md), and if all references to the CoreWebView2Controller go away, the WebView is closed.

## Summary

Members|Description
--|--
[AllowExternalDrop](#allowexternaldrop) | Gets or sets the WebView allow external drop property.
[Bounds](#bounds) | Gets or sets the WebView bounds.
[BoundsMode](#boundsmode) | Gets or sets the WebView bounds mode.
[CoreWebView2](#corewebview2) | Gets the [CoreWebView2](corewebview2.md) associated with this CoreWebView2Controller.
[DefaultBackgroundColor](#defaultbackgroundcolor) | Gets or sets the WebView default background color.
[IsBrowserHitTransparent](#isbrowserhittransparent) | 
[IsVisible](#isvisible) | Determines whether to show or hide the WebView.
[ParentWindow](#parentwindow) | Gets the parent window provided by the app or sets the parent window that this WebView is using to render content.
[RasterizationScale](#rasterizationscale) | Gets or sets the WebView rasterization scale.
[ShouldDetectMonitorScaleChanges](#shoulddetectmonitorscalechanges) | Determines whether the WebView will detect monitor scale changes.
[ZoomFactor](#zoomfactor) | Gets or sets the zoom factor for the WebView.
[Close](#close) | Closes the WebView and cleans up the underlying browser instance.
[MoveFocus](#movefocus) | Moves focus into WebView.
[NotifyParentWindowPositionChanged](#notifyparentwindowpositionchanged) | Tells WebView that the main WebView parent (or any ancestor) HWND moved.
[SetBoundsAndZoomFactor](#setboundsandzoomfactor) | Updates [CoreWebView2Controller.Bounds](corewebview2controller.md#bounds) and [CoreWebView2Controller.ZoomFactor](corewebview2controller.md#zoomfactor) properties at the same time.
[AcceleratorKeyPressed](#acceleratorkeypressed) | AcceleratorKeyPressed is raised when an accelerator key or key combo is pressed or released while the WebView is focused.
[GotFocus](#gotfocus) | GotFocus is raised when WebView gets focus.
[LostFocus](#lostfocus) | LostFocus is raised when WebView loses focus.
[MoveFocusRequested](#movefocusrequested) | MoveFocusRequested is raised when user tries to tab out of the WebView.
[RasterizationScaleChanged](#rasterizationscalechanged) | RasterizationScaleChanged is raised when the [CoreWebView2Controller.RasterizationScale](corewebview2controller.md#rasterizationscale) property changes.
[ZoomFactorChanged](#zoomfactorchanged) | ZoomFactorChanged is raised when the [CoreWebView2Controller.ZoomFactor](corewebview2controller.md#zoomfactor) property changes.

## Properties

### AllowExternalDrop

>  bool AllowExternalDrop

Gets or sets the WebView allow external drop property.
The AllowExternalDrop is to configure the capability that dropping files into webview2 is allowed or permitted. The default value is true.

### Bounds

>  [Rect](/uwp/api/Windows.Foundation.Rect) Bounds

Gets or sets the WebView bounds.
Bounds are relative to the [CoreWebView2Controller.ParentWindow](corewebview2controller.md#parentwindow). The app has two ways to position a WebView:

- Create a child HWND that is the WebView parent HWND. Position the window where the WebView should be. Use (0, 0) for the top-left corner (the offset) of the Bounds of the WebView.
- Use the top-most window of the app as the WebView parent HWND. For example, to position ebView correctly in the app, set the top-left corner of the Bounds of the WebView.

The values of Bounds are limited by the coordinate space of the host.

### BoundsMode

>  [CoreWebView2BoundsMode](corewebview2boundsmode.md) BoundsMode

Gets or sets the WebView bounds mode.
BoundsMode affects how setting the [CoreWebView2Controller.Bounds](corewebview2controller.md#bounds) and [CoreWebView2Controller.RasterizationScale](corewebview2controller.md#rasterizationscale) properties work. Bounds mode can either be in [CoreWebView2BoundsMode](corewebview2boundsmode.md).UseRawPixels mode or [CoreWebView2BoundsMode](corewebview2boundsmode.md).UseRasterizationScale mode.

### CoreWebView2

> readonly  [CoreWebView2](corewebview2.md) CoreWebView2

Gets the [CoreWebView2](corewebview2.md) associated with this CoreWebView2Controller.

### DefaultBackgroundColor

>  [Color](/uwp/api/Windows.UI.Color) DefaultBackgroundColor

Gets or sets the WebView default background color.
The `DefaultBackgroundColor` is the color that renders underneath all web content. This means WebView renders this color when there is no web content loaded such as before the initial navigation or between navigations. This also means web pages with undefined css background properties or background properties containing transparent pixels will render their contents over this color. Web pages with defined and opaque background properties that span the page will obscure the `DefaultBackgroundColor` and display normally. The default value for this property is white to resemble the native browser experience. Currently this API only supports opaque colors and transparency. It will fail for colors with alpha values that don't equal 0 or 255 ie. translucent colors are not supported. It also does not support transparency on Windows 7. On Windows 7, setting DefaultBackgroundColor to a Color with an Alpha value other than 255 will result in failure. On any OS above Win7, choosing a transparent color will result in showing hosting app content. This means webpages without explicit background properties defined will render web content over hosting app content.
This property may also be set via the `WEBVIEW2_DEFAULT_BACKGROUND_COLOR` environment variable. There is a known issue with background color where just setting the color by property can still leave the app with a white flicker before the `DefaultBackgroundColor` property takes effect. Setting the color via environment variable solves this issue. The value must be a hex value that can optionally prepend a 0x. The value must account for the alpha value which is represented by the first 2 digits. So any hex value fewer than 8 digits will assume a prepended 00 to the hex value and result in a transparent color. `DefaultBackgroundColor` will return the result of this environment variable even if it has not been set directly. This environment variable can only set the `DefaultBackgroundColor` once. Subsequent updates to background color must be done by setting the property.

### IsBrowserHitTransparent

> readonly  bool IsBrowserHitTransparent

### IsVisible

>  bool IsVisible

Determines whether to show or hide the WebView.
If `IsVisible` is set to `false`, the WebView is transparent and is not rendered. However, this does not affect the window containing the WebView (the `ParentWindow` parameter that was passed to [CoreWebView2Environment.CreateCoreWebView2ControllerAsync](corewebview2environment.md#createcorewebview2controllerasync)).
WebView as a child window does not get window messages when the top window is minimized or restored. For performance reasons, developers should set the `IsVisible` property of the WebView to `false` when the app window is minimized and back to `true` when the app window is restored. The app window does this by handling `SIZE_MINIMIZED` and `SIZE_RESTORED` command upon receiving `WM_SIZE` message. There are CPU and memory benefits when the page is hidden. For instance Chromium has code that throttles activities on the page like animations and some tasks are run less frequently. Similarly, WebView2 will purge some caches to reduce memory usage.

### ParentWindow

>  [CoreWebView2ControllerWindowReference](corewebview2controllerwindowreference.md) ParentWindow

Gets the parent window provided by the app or sets the parent window that this WebView is using to render content.
It initially returns the `ParentWindow` passed into [CoreWebView2Environment.CreateCoreWebView2ControllerAsync](corewebview2environment.md#createcorewebview2controllerasync). Setting the property causes the WebView to re-parent the main WebView window to the newly provided window.

### RasterizationScale

>  double RasterizationScale

Gets or sets the WebView rasterization scale.
The rasterization scale is the combination of the monitor DPI scale and text scaling set by the user. This value should be updated when the DPI scale of the app's top level window changes (i.e. monitor DPI scale changes or the window changes monitor) or when the text scale factor of the system changes.
Rasterization scale applies to the WebView content, as well as popups, context menus, scroll bars, and so on. Normal app scaling scenarios should use the [CoreWebView2Controller.ZoomFactor](corewebview2controller.md#zoomfactor) property or [CoreWebView2Controller.SetBoundsAndZoomFactor](corewebview2controller.md#setboundsandzoomfactor) method.

### ShouldDetectMonitorScaleChanges

>  bool ShouldDetectMonitorScaleChanges

Determines whether the WebView will detect monitor scale changes.
ShouldDetectMonitorScaleChanges property determines whether the WebView attempts to track monitor DPI scale changes. When true, the WebView will track monitor DPI scale changes, update the [CoreWebView2Controller.RasterizationScale](corewebview2controller.md#rasterizationscale) property, and fire [CoreWebView2Controller.RasterizationScaleChanged](corewebview2controller.md#rasterizationscalechanged) event. When `false`, the WebView will not track monitor DPI scale changes, and the app must update the [CoreWebView2Controller.RasterizationScale](corewebview2controller.md#rasterizationscale) property itself. [CoreWebView2Controller.RasterizationScaleChanged](corewebview2controller.md#rasterizationscalechanged) event will never raise when ShouldDetectMonitorScaleChanges is false. Apps that want to set their own rasterization scale should set this property to false to avoid the WebView2 updating the [CoreWebView2Controller.RasterizationScale](corewebview2controller.md#rasterizationscale) property to match the monitor DPI scale.

### ZoomFactor

>  double ZoomFactor

Gets or sets the zoom factor for the WebView.
Note that changing zoom factor may cause `window.innerWidth` or `window.innerHeight` and page layout to change. A zoom factor that is applied by the host by setting this ZoomFactor property becomes the new default zoom for the WebView. This zoom factor applies across navigations and is the zoom factor WebView is returned to when the user presses Ctrl+0. When the zoom factor is changed by the user (resulting in the app receiving [CoreWebView2Controller.ZoomFactorChanged](corewebview2controller.md#zoomfactorchanged)), that zoom applies only for the current page. Any user applied zoom is only for the current page and is reset on a navigation. Specifying a ZoomFactor less than or equal to 0 is not allowed. WebView also has an internal supported zoom factor range. When a specified zoom factor is out of that range, it is normalized to be within the range, and a [CoreWebView2Controller.ZoomFactorChanged](corewebview2controller.md#zoomfactorchanged) event is raised for the real applied zoom factor. When this range normalization happens, this reports the zoom factor specified during the previous modification of the ZoomFactor property until the [CoreWebView2Controller.ZoomFactorChanged](corewebview2controller.md#zoomfactorchanged) event is received after WebView applies the normalized zoom factor.



## Methods

### Close

> void Close()

Closes the WebView and cleans up the underlying browser instance.
Cleaning up the browser instance releases the resources powering the WebView. The browser instance is shut down if no other WebViews are using it.

After running Close, all methods fail and event handlers stop running. Specifically, the WebView releases the associated references to any associated event handlers when Close is run.

Close is implicitly run when the CoreWebView2Controller loses the final reference and is destructed. But it is best practice to explicitly run Close to avoid any accidental cycle of references between the WebView and the app code. Specifically, if you capture a reference to the WebView in an event handler you create a reference cycle between the WebView and the event handler. Run Close to break the cycle by releasing all event handlers. But to avoid the situation, it is best to both explicitly run Close on the WebView and to not capture a reference to the WebView to ensure the WebView is cleaned up correctly. Close is synchronous and won't trigger the `beforeunload` event.



### MoveFocus

> void MoveFocus([CoreWebView2MoveFocusReason](corewebview2movefocusreason.md) reason)

Moves focus into WebView.
WebView will get focus and focus will be set to correspondent element in the page hosted in the WebView. For [CoreWebView2MoveFocusReason](corewebview2movefocusreason.md).Programmatic reason, focus is set to previously focused element or the default element if no previously focused element exists. For [CoreWebView2MoveFocusReason](corewebview2movefocusreason.md).Next reason, focus is set to the first element. For [CoreWebView2MoveFocusReason](corewebview2movefocusreason.md).Previous reason, focus is set to the last element. WebView changes focus through user interaction including selecting into a WebView or Tab into it. For tabbing, the app runs MoveFocus with [CoreWebView2MoveFocusReason](corewebview2movefocusreason.md).Next or [CoreWebView2MoveFocusReason](corewebview2movefocusreason.md).Previous to align with Tab and Shift+Tab respectively when it decides the WebView is the next tabbable element.



### NotifyParentWindowPositionChanged

> void NotifyParentWindowPositionChanged()

Tells WebView that the main WebView parent (or any ancestor) HWND moved.
This is a notification separate from [CoreWebView2Controller.Bounds](corewebview2controller.md#bounds). This is needed for accessibility and certain dialogs in WebView to work correctly.



### SetBoundsAndZoomFactor

> void SetBoundsAndZoomFactor([Rect](/uwp/api/Windows.Foundation.Rect) Bounds, double ZoomFactor)

Updates [CoreWebView2Controller.Bounds](corewebview2controller.md#bounds) and [CoreWebView2Controller.ZoomFactor](corewebview2controller.md#zoomfactor) properties at the same time.
This operation is atomic from the perspective of the host. After returning from this function, the [CoreWebView2Controller.Bounds](corewebview2controller.md#bounds) and [CoreWebView2Controller.ZoomFactor](corewebview2controller.md#zoomfactor) properties are both updated if the function is successful, or neither is updated if the function fails. If [CoreWebView2Controller.Bounds](corewebview2controller.md#bounds) and [CoreWebView2Controller.ZoomFactor](corewebview2controller.md#zoomfactor) are both updated by the same scale (for example, [CoreWebView2Controller.Bounds](corewebview2controller.md#bounds) and [CoreWebView2Controller.ZoomFactor](corewebview2controller.md#zoomfactor) are both doubled), then the page does not display a change in `window.innerWidth` or `window.innerHeight` and the WebView renders the content at the new size and zoom without intermediate renderings. This function also updates just one of [CoreWebView2Controller.ZoomFactor](corewebview2controller.md#zoomfactor) or [CoreWebView2Controller.Bounds](corewebview2controller.md#bounds) by passing in the new value for one and the current value for the other.




## Events

### AcceleratorKeyPressed

AcceleratorKeyPressed is raised when an accelerator key or key combo is pressed or released while the WebView is focused.
A key is considered an accelerator if either of the following conditions are true:

- Ctrl or Alt is currently being held.
- The pressed key does not map to a character.

A few specific keys are never considered accelerators, such as Shift. The Escape key is always considered an accelerator.

Autorepeated key events caused by holding the key down will also raise this event. Filter out the auto-repeated key events by verifying [CoreWebView2AcceleratorKeyPressedEventArgs.KeyEventLParam](corewebview2acceleratorkeypressedeventargs.md#keyeventlparam) or [CoreWebView2AcceleratorKeyPressedEventArgs.PhysicalKeyStatus](corewebview2acceleratorkeypressedeventargs.md#physicalkeystatus).

In windowed mode, this event is synchronous. Until you set [CoreWebView2AcceleratorKeyPressedEventArgs.Handled](corewebview2acceleratorkeypressedeventargs.md#handled) to `true` or the event handler returns, the browser process is blocked and outgoing cross-process COM calls will fail with RPC_E_CANTCALLOUT_ININPUTSYNCCALL. All [CoreWebView2](corewebview2.md) methods work, however.

In windowless mode, the event is asynchronous. Further input do not reach the browser until the event handler returns or [CoreWebView2AcceleratorKeyPressedEventArgs.Handled](corewebview2acceleratorkeypressedeventargs.md#handled) is set to `true`, but the browser process is not blocked, and outgoing COM calls work normally.

It is recommended to set [CoreWebView2AcceleratorKeyPressedEventArgs.Handled](corewebview2acceleratorkeypressedeventargs.md#handled) to `true` as early as you are able to know that you want to handle the accelerator key.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2Controller, [CoreWebView2AcceleratorKeyPressedEventArgs](corewebview2acceleratorkeypressedeventargs.md)&gt;

### GotFocus

GotFocus is raised when WebView gets focus.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2Controller, Object&gt;

### LostFocus

LostFocus is raised when WebView loses focus.
In the case where [CoreWebView2Controller.MoveFocusRequested](corewebview2controller.md#movefocusrequested) event is raised, the focus is still on WebView when [CoreWebView2Controller.MoveFocusRequested](corewebview2controller.md#movefocusrequested) event is raised. LostFocus is only raised afterwards when code of the app or default action of [CoreWebView2Controller.MoveFocusRequested](corewebview2controller.md#movefocusrequested) event sets focus away from WebView.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2Controller, Object&gt;

### MoveFocusRequested

MoveFocusRequested is raised when user tries to tab out of the WebView.
The focus of the WebView has not changed when this event is raised.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2Controller, [CoreWebView2MoveFocusRequestedEventArgs](corewebview2movefocusrequestedeventargs.md)&gt;

### RasterizationScaleChanged

RasterizationScaleChanged is raised when the [CoreWebView2Controller.RasterizationScale](corewebview2controller.md#rasterizationscale) property changes.
The event is raised when the Webview detects that the monitor DPI scale has changed, [CoreWebView2Controller.ShouldDetectMonitorScaleChanges](corewebview2controller.md#shoulddetectmonitorscalechanges) is true, and the Webview has changed the [CoreWebView2Controller.RasterizationScale](corewebview2controller.md#rasterizationscale) property.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2Controller, Object&gt;

### ZoomFactorChanged

ZoomFactorChanged is raised when the [CoreWebView2Controller.ZoomFactor](corewebview2controller.md#zoomfactor) property changes.
The event may be raised because the [CoreWebView2Controller.ZoomFactor](corewebview2controller.md#zoomfactor) property was modified, or due to the user manually modifying the zoom. When it is modified using the [CoreWebView2Controller.ZoomFactor](corewebview2controller.md#zoomfactor) property, the internal zoom factor is updated immediately and no ZoomFactorChanged event is raised. WebView associates the last used zoom factor for each site. It is possible for the zoom factor to change when navigating to a different page. When the zoom factor changes due to a navigation change, the ZoomFactorChanged event is raised right after the [CoreWebView2.ContentLoading](corewebview2.md#contentloading) event.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2Controller, Object&gt;

