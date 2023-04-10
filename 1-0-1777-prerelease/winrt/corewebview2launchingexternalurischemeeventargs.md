---
description: Event args for the CoreWebView2.LaunchingExternalUriScheme event.
title: CoreWebView2LaunchingExternalUriSchemeEventArgs
ms.date: 04/10/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2LaunchingExternalUriSchemeEventArgs
---

# CoreWebView2LaunchingExternalUriSchemeEventArgs Class



Event args for the [CoreWebView2.LaunchingExternalUriScheme](corewebview2.md#launchingexternalurischeme) event.

## Summary

Members|Description
--|--
[Cancel](#cancel) | Determines whether to cancel the navigation.
[InitiatingOrigin](#initiatingorigin) | Gets the origin initiating the external URI scheme launch.
[IsUserInitiated](#isuserinitiated) | `true` when the launching external URI scheme request was initiated through a user gesture.
[Uri](#uri) | Gets the URI with the external URI scheme to be launched.
[GetDeferral](#getdeferral) | Gets a Deferral object and puts the event into a deferred state.

## Properties

### Cancel

>  bool Cancel

Determines whether to cancel the navigation.

### InitiatingOrigin

> readonly  string InitiatingOrigin

Gets the origin initiating the external URI scheme launch.
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
