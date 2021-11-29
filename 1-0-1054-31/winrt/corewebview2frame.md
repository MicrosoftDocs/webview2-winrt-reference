---
description: CoreWebView2Frame provides direct access to the iframes information and handling.
title: CoreWebView2Frame
ms.date: 11/29/2021
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2Frame
---

# CoreWebView2Frame Class



CoreWebView2Frame provides direct access to the iframes information and handling.

## Summary

Members|Description
--|--
[Name](#name) | The name of the iframe from the iframe html tag declaring it.
[IsDestroyed](#isdestroyed) | Check whether a frame is destroyed. Returns true during the [CoreWebView2Frame.Destroyed](corewebview2frame.md#destroyed) event.
[RemoveHostObjectFromScript](#removehostobjectfromscript) | Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the iframe.
[Destroyed](#destroyed) | Destroyed event is raised when the iframe corresponding to this CoreWebView2Frame object is removed or the document containing that iframe is destroyed.
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

Destroyed event is raised when the iframe corresponding to this CoreWebView2Frame object is removed or the document containing that iframe is destroyed.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2Frame, Object&gt;

### NameChanged

NameChanged is raised when the iframe changes its `window.name` property.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2Frame, Object&gt;



## Referenced by

- [CoreWebView2FrameCreatedEventArgs](corewebview2framecreatedeventargs.md)
