---
description: Event args for the CoreWebView2.LaunchingExternalUriScheme event.
title: CoreWebView2LaunchingExternalUriSchemeEventArgs
ms.date: 10-29-2026
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
[Cancel](#cancel) | Determines whether to cancel the external URI scheme launch.
[InitiatingOrigin](#initiatingorigin) | Gets the origin initiating the external URI scheme launch.
[IsUserInitiated](#isuserinitiated) | `true` when the request was initiated through a WebView2 API, or when a renderer-initiated request reports a user gesture correlated with recent browser-observed user activation.
[Uri](#uri) | Gets the URI with the external URI scheme to be launched.
[GetDeferral](#getdeferral) | Gets a Deferral object and puts the event into a deferred state.

## Properties

### Cancel

>  bool Cancel

Determines whether to cancel the external URI scheme launch.

The event handler may set this property to `true` to cancel the external URI scheme launch. If set to `true`, the external URI scheme will not be launched, and the default dialog is not displayed. This property can be used to replace the normal handling of launching an external URI scheme. The initial value of the `Cancel` property is `false`.

### InitiatingOrigin

> readonly  string InitiatingOrigin

Gets the origin initiating the external URI scheme launch.

The origin will be an empty string if the request is initiated by calling [CoreWebView2.Navigate](corewebview2.md#navigate) on the external URI scheme. If a script initiates the navigation, the `InitiatingOrigin` will be the top-level document's [CoreWebView2.Source](corewebview2.md#source). If the request is initiated from a child frame, the `InitiatingOrigin` will be the source of that child frame. If the `InitiatingOrigin` is [opaque](https://html.spec.whatwg.org/multipage/origin.html#concept-origin-opaque), the `InitiatingOrigin` reported in the event args will be its precursor origin. The precursor origin is the origin that created the opaque origin. For example, if a frame on example.com opens a subframe with a different opaque origin, the subframe's precursor origin is example.com.

### IsUserInitiated

> readonly  bool IsUserInitiated

`true` when the request was initiated through a WebView2 API, or when a renderer-initiated request reports a user gesture correlated with recent browser-observed user activation.

This property indicates activation correlation, not that the activation caused the request or that the user intended to access the associated resource. Applications should validate the URI, scheme, and [CoreWebView2LaunchingExternalUriSchemeEventArgs.InitiatingOrigin](corewebview2launchingexternalurischemeeventargs.md#initiatingorigin).

### Uri

> readonly  string Uri

Gets the URI with the external URI scheme to be launched.



## Methods

### GetDeferral

> [Deferral](/uwp/api/Windows.Foundation.Deferral) GetDeferral()

Gets a Deferral object and puts the event into a deferred state.
Use this to complete the launching external URI scheme request at a later time.






## Referenced by

- [CoreWebView2](corewebview2.md)
