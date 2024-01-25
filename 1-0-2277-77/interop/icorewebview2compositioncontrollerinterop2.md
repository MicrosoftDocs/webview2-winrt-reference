---
description: This interface is the continuation of the ICoreWebView2CompositionControllerInterop interface to manage drag and drop.
title: WebView2 WinRT COM ICoreWebView2CompositionControllerInterop2
ms.date: 01/29/2024
keywords: IWebView2, IWebView2WebView, webview2, webview, winrt, interop, edge, ICoreWebView2, ICoreWebView2Controller, browser control, edge html, ICoreWebView2CompositionControllerInterop2
---

# interface ICoreWebView2CompositionControllerInterop2

```
interface ICoreWebView2CompositionControllerInterop2
  : public ICoreWebView2CompositionControllerInterop
```

This interface is the continuation of the [ICoreWebView2CompositionControllerInterop](icorewebview2compositioncontrollerinterop.md) interface to manage drag and drop.

## Summary

 Members                        | Descriptions
--------------------------------|---------------------------------------------
[DragEnter](#dragenter) | This function corresponds to [IDropTarget::DragEnter](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter).
[DragLeave](#dragleave) | This function corresponds to [IDropTarget::DragLeave](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragleave).
[DragOver](#dragover) | This function corresponds to [IDropTarget::DragOver](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover).
[Drop](#drop) | This function corresponds to [IDropTarget::Drop](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop).

## Members

#### DragEnter

This function corresponds to [IDropTarget::DragEnter](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragenter).

> public HRESULT [DragEnter](#dragenter)(IDataObject * dataObject, DWORD keyState, POINT point, DWORD * effect)

This function has a dependency on AllowExternalDrop property of CoreWebView2Controller and return E_FAIL to callers to indicate this operation is not allowed if AllowExternalDrop property is set to false.

The hosting application must register as an IDropTarget and implement and forward DragEnter calls to this function.

point parameter must be modified to include the WebView's offset and be in the WebView's client coordinates (Similar to how SendMouseInput works).

```cpp
HRESULT DropTarget::DragEnter(
    IDataObject* dataObject, DWORD keyState, POINTL cursorPosition, DWORD* effect)
{
    POINT point = {cursorPosition.x, cursorPosition.y};
    // Convert the screen point to client coordinates add the WebView's offset.
    m_viewComponent->OffsetPointToWebView(&point);
    return m_webViewCompositionController3->DragEnter(dataObject, keyState, point, effect);
}
```

#### DragLeave

This function corresponds to [IDropTarget::DragLeave](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragleave).

> public HRESULT [DragLeave](#dragleave)()

This function has a dependency on AllowExternalDrop property of CoreWebView2Controller and return E_FAIL to callers to indicate this operation is not allowed if AllowExternalDrop property is set to false.

The hosting application must register as an IDropTarget and implement and forward DragLeave calls to this function.

```cpp
HRESULT DropTarget::DragLeave()
{
    return m_webViewCompositionController3->DragLeave();
}
```

#### DragOver

This function corresponds to [IDropTarget::DragOver](/windows/win32/api/oleidl/nf-oleidl-idroptarget-dragover).

> public HRESULT [DragOver](#dragover)(DWORD keyState, POINT point, DWORD * effect)

This function has a dependency on AllowExternalDrop property of CoreWebView2Controller and return E_FAIL to callers to indicate this operation is not allowed if AllowExternalDrop property is set to false.

The hosting application must register as an IDropTarget and implement and forward DragOver calls to this function.

point parameter must be modified to include the WebView's offset and be in the WebView's client coordinates (Similar to how SendMouseInput works).

```cpp
HRESULT DropTarget::DragOver(DWORD keyState, POINTL cursorPosition, DWORD* effect)
{
    POINT point = {cursorPosition.x, cursorPosition.y};
    // Convert the screen point to client coordinates add the WebView's offset.
    // This returns whether the resultant point is over the WebView visual.
    m_viewComponent->OffsetPointToWebView(&point);
    return m_webViewCompositionController3->DragOver(keyState, point, effect);
}
```

#### Drop

This function corresponds to [IDropTarget::Drop](/windows/win32/api/oleidl/nf-oleidl-idroptarget-drop).

> public HRESULT [Drop](#drop)(IDataObject * dataObject, DWORD keyState, POINT point, DWORD * effect)

This function has a dependency on AllowExternalDrop property of CoreWebView2Controller and return E_FAIL to callers to indicate this operation is not allowed if AllowExternalDrop property is set to false.

The hosting application must register as an IDropTarget and implement and forward Drop calls to this function.

point parameter must be modified to include the WebView's offset and be in the WebView's client coordinates (Similar to how SendMouseInput works).

```cpp
HRESULT DropTarget::Drop(
    IDataObject* dataObject, DWORD keyState, POINTL cursorPosition, DWORD* effect)
{
    POINT point = {cursorPosition.x, cursorPosition.y};
    // Convert the screen point to client coordinates add the WebView's offset.
    // This returns whether the resultant point is over the WebView visual.
    m_viewComponent->OffsetPointToWebView(&point);
    return m_webViewCompositionController3->Drop(dataObject, keyState, point, effect);
}
```

