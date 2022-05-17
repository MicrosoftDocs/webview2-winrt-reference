---
description: Represents the information regarding the context menu target. Includes the context selected and the appropriate data used for the actions of a context menu.
title: CoreWebView2ContextMenuTarget
ms.date: 05/17/2022
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ContextMenuTarget
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
