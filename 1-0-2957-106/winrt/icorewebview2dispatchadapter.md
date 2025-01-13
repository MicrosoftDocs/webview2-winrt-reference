---
title: ICoreWebView2DispatchAdapter
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/13/2025
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, ICoreWebView2DispatchAdapter
---

# interface ICoreWebView2DispatchAdapter



Interface to create IDispatch implementing adapter classes for WinRT runtime classes to work with [CoreWebView2.AddHostObjectToScript](corewebview2.md#addhostobjecttoscript).

## Summary

Members|Description
--|--
[Clean](#clean) | Release references to WinRT objects used with objects produced from [ICoreWebView2DispatchAdapter.WrapObject](icorewebview2dispatchadapter.md#wrapobject) or [ICoreWebView2DispatchAdapter.WrapNamedObject](icorewebview2dispatchadapter.md#wrapnamedobject), directly or indirectly, that are no longer necessary to retain.
[UnwrapObject](#unwrapobject) | Given an object returned by [ICoreWebView2DispatchAdapter.WrapObject](icorewebview2dispatchadapter.md#wrapobject), this method returns the original WinRT object used in the call to [ICoreWebView2DispatchAdapter.WrapObject](icorewebview2dispatchadapter.md#wrapobject).
[WrapNamedObject](#wrapnamedobject) | Given a named WinRT namespace, runtimeclass with constructor's name, static API's name, or enum name, this method returns an object that implements IDispatch representing that named entity.
[WrapObject](#wrapobject) | Given a WinRT object, this method returns an object that implements IDispatch representing that object.



## Methods

### Clean

> void Clean()

Release references to WinRT objects used with objects produced from [ICoreWebView2DispatchAdapter.WrapObject](icorewebview2dispatchadapter.md#wrapobject) or [ICoreWebView2DispatchAdapter.WrapNamedObject](icorewebview2dispatchadapter.md#wrapnamedobject), directly or indirectly, that are no longer necessary to retain.



### UnwrapObject

> Object UnwrapObject(Object wrapped)

Given an object returned by [ICoreWebView2DispatchAdapter.WrapObject](icorewebview2dispatchadapter.md#wrapobject), this method returns the original WinRT object used in the call to [ICoreWebView2DispatchAdapter.WrapObject](icorewebview2dispatchadapter.md#wrapobject).



### WrapNamedObject

> Object WrapNamedObject(string name, [ICoreWebView2DispatchAdapter](icorewebview2dispatchadapter.md) adapter)

Given a named WinRT namespace, runtimeclass with constructor's name, static API's name, or enum name, this method returns an object that implements IDispatch representing that named entity.
The adapter parameter is this DispatchAdapter or a parent DispatchAdapter.



### WrapObject

> Object WrapObject(Object unwrapped, [ICoreWebView2DispatchAdapter](icorewebview2dispatchadapter.md) adapter)

Given a WinRT object, this method returns an object that implements IDispatch representing that object.
The adapter parameter is this DispatchAdapter or a parent DispatchAdapter.






## Referenced by

- [CoreWebView2Settings](corewebview2settings.md)
