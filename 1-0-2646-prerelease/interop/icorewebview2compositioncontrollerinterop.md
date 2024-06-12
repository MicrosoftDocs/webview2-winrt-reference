---
description: Interop interface for the CoreWebView2CompositionController WinRT object to allow WinRT end developers to be able to use the COM interfaces as parameters for some methods.
title: WebView2 WinRT COM ICoreWebView2CompositionControllerInterop
ms.date: 06/19/2024
keywords: IWebView2, IWebView2WebView, webview2, webview, winrt, interop, edge, ICoreWebView2, ICoreWebView2Controller, browser control, edge html, ICoreWebView2CompositionControllerInterop
topic_type: 
- APIRef
api_name:
- ICoreWebView2CompositionControllerInterop
- ICoreWebView2CompositionControllerInterop.get_AutomationProvider
- ICoreWebView2CompositionControllerInterop.get_RootVisualTarget
- ICoreWebView2CompositionControllerInterop.put_RootVisualTarget
api_type:
- COM
api_location:
- embeddedbrowserwebview.dll
---

# interface ICoreWebView2CompositionControllerInterop

```
interface ICoreWebView2CompositionControllerInterop
  : public IUnknown
```

Interop interface for the CoreWebView2CompositionController WinRT object to allow WinRT end developers to be able to use the COM interfaces as parameters for some methods.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
[get_AutomationProvider](#get_automationprovider) | Returns the UI Automation Provider for the WebView.
[get_RootVisualTarget](#get_rootvisualtarget) | The RootVisualTarget is a visual in the hosting app's visual tree.
[put_RootVisualTarget](#put_rootvisualtarget) | Set the RootVisualTarget property.

This interface is implemented by the Microsoft.Web.WebView2.Core.CoreWebView2CompositionController runtime class.

## Members

#### get_AutomationProvider

Returns the UI Automation Provider for the WebView.

> public HRESULT [get_AutomationProvider](#get_automationprovider)(IUnknown ** provider)

See the documentation for ICoreWebView2CompositionController::AutomationProvider for more information.

#### get_RootVisualTarget

The RootVisualTarget is a visual in the hosting app's visual tree.

> public HRESULT [get_RootVisualTarget](#get_rootvisualtarget)(IUnknown ** target)

This visual is where the WebView2 will connect its visual tree. See the documentation for ICoreWebView2CompositionController::RootVisualTarget for more information.

#### put_RootVisualTarget

Set the RootVisualTarget property.

> public HRESULT [put_RootVisualTarget](#put_rootvisualtarget)(IUnknown * target)

