---
description: Event args for the CoreWebView2.LaunchingExternalUriScheme event.
title: CoreWebView2LaunchingExternalUriSchemeEventArgs
ms.date: 09/03/2026
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2LaunchingExternalUriSchemeEventArgs
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2LaunchingExternalUriSchemeEventArgs
- CoreWebView2LaunchingExternalUriSchemeEventArgs.Cancel
- CoreWebView2LaunchingExternalUriSchemeEventArgs.Handled
- CoreWebView2LaunchingExternalUriSchemeEventArgs.InitiatingOrigin
- CoreWebView2LaunchingExternalUriSchemeEventArgs.IsUserInitiated
- CoreWebView2LaunchingExternalUriSchemeEventArgs.Uri
- CoreWebView2LaunchingExternalUriSchemeEventArgs.GetDeferral
---

# CoreWebView2LaunchingExternalUriSchemeEventArgs Class



Event args for the [CoreWebView2.LaunchingExternalUriScheme](corewebview2.md#launchingexternalurischeme) event.

## Summary

Members|Description
--|--
[Cancel](#cancel) | Determines whether to cancel the navigation.
[Handled](#handled) | Indicates whether a [CoreWebView2Frame](corewebview2frame.md) event handler has handled this [CoreWebView2Frame.LaunchingExternalUriScheme](corewebview2frame.md#launchingexternalurischeme) event. Defaults to `false`.
[InitiatingOrigin](#initiatingorigin) | Gets the origin initiating the external URI scheme launch. If the `InitiatingOrigin` is [opaque](https://html.spec.whatwg.org/multipage/origin.html#concept-origin-opaque), the `InitiatingOrigin` reported in the event args will be its precursor origin. The precursor origin is the origin that created the opaque origin. For example, if a frame on example.com opens a subframe with a different opaque origin, the subframe's precursor origin is example.com.
[IsUserInitiated](#isuserinitiated) | `true` when the launching external URI scheme request was initiated through a user gesture.
[Uri](#uri) | Gets the URI with the external URI scheme to be launched.
[GetDeferral](#getdeferral) | Gets a Deferral object and puts the event into a deferred state.

## Properties

### Cancel

>  bool Cancel

Determines whether to cancel the navigation.

### Handled

>  bool Handled

Indicates whether a [CoreWebView2Frame](corewebview2frame.md) event handler has handled this [CoreWebView2Frame.LaunchingExternalUriScheme](corewebview2frame.md#launchingexternalurischeme) event. Defaults to `false`.
By default, the [CoreWebView2Frame.LaunchingExternalUriScheme](corewebview2frame.md#launchingexternalurischeme) and [CoreWebView2.LaunchingExternalUriScheme](corewebview2.md#launchingexternalurischeme) event handlers are all invoked, with the [CoreWebView2Frame](corewebview2frame.md) event handlers invoked first, innermost frame first for nested iframes. The host may set this property to `true` within a [CoreWebView2Frame](corewebview2frame.md) event handler to prevent the remaining ancestor [CoreWebView2Frame](corewebview2frame.md) and [CoreWebView2](corewebview2.md) event handlers from being invoked. Setting `Handled` has no effect when the event is raised on [CoreWebView2](corewebview2.md); it only suppresses the remaining handlers when set from a frame-level event handler.

### InitiatingOrigin

> readonly  string InitiatingOrigin

Gets the origin initiating the external URI scheme launch. If the `InitiatingOrigin` is [opaque](https://html.spec.whatwg.org/multipage/origin.html#concept-origin-opaque), the `InitiatingOrigin` reported in the event args will be its precursor origin. The precursor origin is the origin that created the opaque origin. For example, if a frame on example.com opens a subframe with a different opaque origin, the subframe's precursor origin is example.com.
The origin will be an empty string if the request is initiated by calling [CoreWebView2.Navigate](corewebview2.md#navigate) on the external URI scheme. If a script initiates the navigation, the `InitiatingOrigin` will be the top-level document's `Source`, i.e. if `window.location` is set to `"calculator://", the `InitiatingOrigin` will be set to `calculator://`. If the request is initiated from a child frame, the `InitiatingOrigin` will be the source of that child frame.

### IsUserInitiated

> readonly  bool IsUserInitiated

`true` when the launching external URI scheme request was initiated through a user gesture.

### Uri

> readonly  string Uri

Gets the URI with the external URI scheme to be launched.



## Methods

### GetDeferral

> [Deferral](/uwp/api/Windows.Foundation.Deferral) GetDeferral()

Gets a Deferral object and puts the event into a deferred state.
Use this to Complete the launching external URI scheme request at a later time.






## Referenced by

- [CoreWebView2](corewebview2.md)
- [CoreWebView2Frame](corewebview2frame.md)
