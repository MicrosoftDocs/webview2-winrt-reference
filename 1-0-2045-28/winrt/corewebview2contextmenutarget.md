---
description: Represents the information regarding the context menu target. Includes the context selected and the appropriate data used for the actions of a context menu.
title: CoreWebView2ContextMenuTarget
ms.date: 09/18/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ContextMenuTarget
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuTarget
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuTarget.FrameUri
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuTarget.HasLinkText
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuTarget.HasLinkUri
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuTarget.HasSelection
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuTarget.HasSourceUri
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuTarget.IsEditable
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuTarget.IsRequestedForMainFrame
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuTarget.Kind
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuTarget.LinkText
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuTarget.LinkUri
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuTarget.PageUri
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuTarget.SelectionText
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuTarget.SourceUri
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuTarget.get_FrameUri
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuTarget.get_HasLinkText
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuTarget.get_HasLinkUri
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuTarget.get_HasSelection
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuTarget.get_HasSourceUri
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuTarget.get_IsEditable
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuTarget.get_IsRequestedForMainFrame
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuTarget.get_Kind
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuTarget.get_LinkText
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuTarget.get_LinkUri
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuTarget.get_PageUri
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuTarget.get_SelectionText
- Microsoft.Web.WebView2.Core.CoreWebView2ContextMenuTarget.get_SourceUri
---

# CoreWebView2ContextMenuTarget Class



Represents the information regarding the context menu target. Includes the context selected and the appropriate data used for the actions of a context menu.

## Summary

Members|Description
--|--
[FrameUri](#frameuri) | Gets the uri of the frame. Will match the [CoreWebView2ContextMenuTarget.PageUri](corewebview2contextmenutarget.md#pageuri) if [CoreWebView2ContextMenuTarget.IsRequestedForMainFrame](corewebview2contextmenutarget.md#isrequestedformainframe) is `true`.
[HasLinkText](#haslinktext) | Returns `true` if the context menu is requested on text element that contains an anchor tag.
[HasLinkUri](#haslinkuri) | Returns `true` if the context menu is requested on HTML containing an anchor tag.
[HasSelection](#hasselection) | Returns `true` if the context menu is requested on a selection.
[HasSourceUri](#hassourceuri) | Returns `true` if the context menu is requested on HTML containing a source uri.
[IsEditable](#iseditable) | Returns `true` if the context menu is requested on an editable component.
[IsRequestedForMainFrame](#isrequestedformainframe) | Returns `true` if the context menu was requested on the main frame and `false` if invoked on another frame.
[Kind](#kind) | Gets the kind of context that the user selected as [CoreWebView2ContextMenuTargetKind](corewebview2contextmenutargetkind.md).
[LinkText](#linktext) | Gets the text of the link (if [CoreWebView2ContextMenuTarget.HasLinkText](corewebview2contextmenutarget.md#haslinktext) is `true`, `null` otherwise).
[LinkUri](#linkuri) | Gets the uri of the link (if [CoreWebView2ContextMenuTarget.HasLinkUri](corewebview2contextmenutarget.md#haslinkuri) is `true`, `null` otherwise).
[PageUri](#pageuri) | Gets the uri of the page.
[SelectionText](#selectiontext) | Gets the selected text (if [CoreWebView2ContextMenuTarget.HasSelection](corewebview2contextmenutarget.md#hasselection) is `true`, `null` otherwise).
[SourceUri](#sourceuri) | Gets the active source uri of element (if [CoreWebView2ContextMenuTarget.HasSourceUri](corewebview2contextmenutarget.md#hassourceuri) is `true`, `null` otherwise).

## Properties

### FrameUri

> readonly  string FrameUri

Gets the uri of the frame. Will match the [CoreWebView2ContextMenuTarget.PageUri](corewebview2contextmenutarget.md#pageuri) if [CoreWebView2ContextMenuTarget.IsRequestedForMainFrame](corewebview2contextmenutarget.md#isrequestedformainframe) is `true`.

### HasLinkText

> readonly  bool HasLinkText

Returns `true` if the context menu is requested on text element that contains an anchor tag.

### HasLinkUri

> readonly  bool HasLinkUri

Returns `true` if the context menu is requested on HTML containing an anchor tag.

### HasSelection

> readonly  bool HasSelection

Returns `true` if the context menu is requested on a selection.

### HasSourceUri

> readonly  bool HasSourceUri

Returns `true` if the context menu is requested on HTML containing a source uri.

### IsEditable

> readonly  bool IsEditable

Returns `true` if the context menu is requested on an editable component.

### IsRequestedForMainFrame

> readonly  bool IsRequestedForMainFrame

Returns `true` if the context menu was requested on the main frame and `false` if invoked on another frame.

### Kind

> readonly  [CoreWebView2ContextMenuTargetKind](corewebview2contextmenutargetkind.md) Kind

Gets the kind of context that the user selected as [CoreWebView2ContextMenuTargetKind](corewebview2contextmenutargetkind.md).

### LinkText

> readonly  string LinkText

Gets the text of the link (if [CoreWebView2ContextMenuTarget.HasLinkText](corewebview2contextmenutarget.md#haslinktext) is `true`, `null` otherwise).

### LinkUri

> readonly  string LinkUri

Gets the uri of the link (if [CoreWebView2ContextMenuTarget.HasLinkUri](corewebview2contextmenutarget.md#haslinkuri) is `true`, `null` otherwise).

### PageUri

> readonly  string PageUri

Gets the uri of the page.

### SelectionText

> readonly  string SelectionText

Gets the selected text (if [CoreWebView2ContextMenuTarget.HasSelection](corewebview2contextmenutarget.md#hasselection) is `true`, `null` otherwise).

### SourceUri

> readonly  string SourceUri

Gets the active source uri of element (if [CoreWebView2ContextMenuTarget.HasSourceUri](corewebview2contextmenutarget.md#hassourceuri) is `true`, `null` otherwise).






## Referenced by

- [CoreWebView2ContextMenuRequestedEventArgs](corewebview2contextmenurequestedeventargs.md)
