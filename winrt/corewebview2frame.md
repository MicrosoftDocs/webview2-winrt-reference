---
title: CoreWebView2Frame
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/12/2021
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2Frame
---

# runtimeClass CoreWebView2Frame



CoreWebView2Frame provides direct access to the iframes information and handling.

## Summary

Members|Description
--|--
[Name](#name) | The name of the iframe from the iframe html tag declaring it.
[IsDestroyed](#isdestroyed) | Check whether a frame is destroyed. Returns true during the [CoreWebView2Frame.Destroyed](corewebview2frame.md#destroyed) event.
[RemoveHostObjectFromScript](#removehostobjectfromscript) | Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the iframe.
[Destroyed](#destroyed) | Destroyed event is raised when the iframe corresponding to this [CoreWebView2Frame](corewebview2frame.md) object is removed or the document containing that iframe is destroyed.
[NameChanged](#namechanged) | NameChanged is raised when the iframe changes its `window.name` property.

## Properties

### Name

> readonly  string Name

The name of the iframe from the iframe html tag declaring it.



## Methods

### IsDestroyed

> int IsDestroyed()

Check whether a frame is destroyed. Returns true during the [CoreWebView2Frame.Destroyed](corewebview2frame.md#destroyed) event.



### RemoveHostObjectFromScript

> void RemoveHostObjectFromScript(string name)

Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the iframe.

While new access attempts are denied, if the object is already obtained by JavaScript code in the iframe, the JavaScript code continues to have access to that object. Calling this method for a name that is already removed or was never added fails. If the iframe is destroyed this method will return fail also.




## Events

### Destroyed

Destroyed event is raised when the iframe corresponding to this [CoreWebView2Frame](corewebview2frame.md) object is removed or the document containing that iframe is destroyed.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2Frame](corewebview2frame.md), Object&gt;

### NameChanged

NameChanged is raised when the iframe changes its `window.name` property.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2Frame](corewebview2frame.md), Object&gt;

## Referenced by

- [CoreWebView2FrameCreatedEventArgs](corewebview2framecreatedeventargs.md)
