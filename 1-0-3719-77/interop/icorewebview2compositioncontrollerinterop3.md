---
description: Interop interface for the CoreWebView2CompositionController WinRT object to allow WinRT end developers to be able to access the COM interface arguments.
title: WebView2 WinRT COM ICoreWebView2CompositionControllerInterop3
ms.date: 01/14/2026
keywords: IWebView2, IWebView2WebView, webview2, webview, winrt, interop, edge, ICoreWebView2, ICoreWebView2Controller, browser control, edge html, ICoreWebView2CompositionControllerInterop3
---

# interface ICoreWebView2CompositionControllerInterop3

```
interface ICoreWebView2CompositionControllerInterop3
  : public ICoreWebView2CompositionControllerInterop2
```

Interop interface for the CoreWebView2CompositionController WinRT object to allow WinRT end developers to be able to access the COM interface arguments.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
[add_DragStarting](#add_dragstarting) | Adds an event handler for the `DragStarting` event.
[remove_DragStarting](#remove_dragstarting) | Removes an event handler previously added with `add_DragStarting`.

This interface is implemented by the Microsoft.Web.WebView2.Core.CoreWebView2CompositionController runtime class.

## Applies to

Product                         | Introduced
--------------------------------|---------------------------------------------
WebView2 WinRT            |    N/A
WebView2 WinRT Prerelease |    1.0.3712

## Members

#### add_DragStarting

Adds an event handler for the `DragStarting` event.

> public HRESULT [add_DragStarting](#add_dragstarting)(ICoreWebView2DragStartingEventHandler * eventHandler, EventRegistrationToken * token)

`DragStarting` is raised when the WebView2 detects a drag started within the WebView2. This event can be used to override WebView2's default drag starting logic.

#### remove_DragStarting

Removes an event handler previously added with `add_DragStarting`.

> public HRESULT [remove_DragStarting](#remove_dragstarting)(EventRegistrationToken token)

