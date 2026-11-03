---
description: Represents the information regarding the context menu target. Includes the context selected and the appropriate data used for the actions of a context menu.
title: CoreWebView2ContextMenuTarget
ms.date: 10/28/2026
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ContextMenuTarget
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2ContextMenuTarget
- CoreWebView2ContextMenuTarget.FrameUri
- CoreWebView2ContextMenuTarget.HasLinkText
- CoreWebView2ContextMenuTarget.HasLinkUri
- CoreWebView2ContextMenuTarget.HasSelection
- CoreWebView2ContextMenuTarget.HasSourceUri
- CoreWebView2ContextMenuTarget.HasSpellingError
- CoreWebView2ContextMenuTarget.IsEditable
- CoreWebView2ContextMenuTarget.IsRequestedForMainFrame
- CoreWebView2ContextMenuTarget.Kind
- CoreWebView2ContextMenuTarget.LinkText
- CoreWebView2ContextMenuTarget.LinkUri
- CoreWebView2ContextMenuTarget.PageUri
- CoreWebView2ContextMenuTarget.SelectionText
- CoreWebView2ContextMenuTarget.SourceUri
- CoreWebView2ContextMenuTarget.GetSpellCheckSuggestionsAsync
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
[HasSpellingError](#hasspellingerror) | Returns `true` if the context menu target contains a spelling error.
[IsEditable](#iseditable) | Returns `true` if the context menu is requested on an editable component.
[IsRequestedForMainFrame](#isrequestedformainframe) | Returns `true` if the context menu was requested on the main frame and `false` if invoked on another frame.
[Kind](#kind) | Gets the kind of context that the user selected as [CoreWebView2ContextMenuTargetKind](corewebview2contextmenutargetkind.md).
[LinkText](#linktext) | Gets the text of the link (if [CoreWebView2ContextMenuTarget.HasLinkText](corewebview2contextmenutarget.md#haslinktext) is `true`, `null` otherwise).
[LinkUri](#linkuri) | Gets the uri of the link (if [CoreWebView2ContextMenuTarget.HasLinkUri](corewebview2contextmenutarget.md#haslinkuri) is `true`, `null` otherwise).
[PageUri](#pageuri) | Gets the uri of the page.
[SelectionText](#selectiontext) | Gets the selected text (if [CoreWebView2ContextMenuTarget.HasSelection](corewebview2contextmenutarget.md#hasselection) is `true`, `null` otherwise).
[SourceUri](#sourceuri) | Gets the active source uri of element (if [CoreWebView2ContextMenuTarget.HasSourceUri](corewebview2contextmenutarget.md#hassourceuri) is `true`, `null` otherwise).
[GetSpellCheckSuggestionsAsync](#getspellchecksuggestionsasync) | Asynchronously retrieves spelling corrections for the misspelled word associated with the context menu target as a read-only collection of [CoreWebView2SpellCheckSuggestion](corewebview2spellchecksuggestion.md) objects.

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

### HasSpellingError

> readonly  bool HasSpellingError

Returns `true` if the context menu target contains a spelling error.
When `true`, call [CoreWebView2ContextMenuTarget.GetSpellCheckSuggestionsAsync](corewebview2contextmenutarget.md#getspellchecksuggestionsasync) to retrieve the available spelling corrections asynchronously.

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



## Methods

### GetSpellCheckSuggestionsAsync

> [`IAsyncOperation`](/uwp/api/Windows.Foundation.IAsyncOperation-1)&lt;[`IVectorView`](/uwp/api/Windows.Foundation.Collections.IVectorView-1)&lt;[CoreWebView2SpellCheckSuggestion](corewebview2spellchecksuggestion.md)&gt;&gt; GetSpellCheckSuggestionsAsync()

Asynchronously retrieves spelling corrections for the misspelled word associated with the context menu target as a read-only collection of [CoreWebView2SpellCheckSuggestion](corewebview2spellchecksuggestion.md) objects.
Each suggestion's [CoreWebView2SpellCheckSuggestion.SuggestionText](corewebview2spellchecksuggestion.md#suggestiontext) is the correction text. Its [CoreWebView2SpellCheckSuggestion.CommandId](corewebview2spellchecksuggestion.md#commandid) can be passed to [CoreWebView2ContextMenuRequestedEventArgs.SelectedCommandId](corewebview2contextmenurequestedeventargs.md#selectedcommandid) to apply the correction, using the same commanding path as built-in context menu items.

Before awaiting this method, set [CoreWebView2ContextMenuRequestedEventArgs.Handled](corewebview2contextmenurequestedeventargs.md#handled) to `true` and obtain a deferral by calling [CoreWebView2ContextMenuRequestedEventArgs.GetDeferral](corewebview2contextmenurequestedeventargs.md#getdeferral). Hold the deferral until the custom menu closes. If a suggestion is selected, assign its command ID to [CoreWebView2ContextMenuRequestedEventArgs.SelectedCommandId](corewebview2contextmenurequestedeventargs.md#selectedcommandid) before completing the deferral. Complete the deferral even if no suggestion is selected.

The returned operation may already be complete if suggestions are ready. Otherwise, it completes when they become available. Multiple concurrent calls are supported. Each operation receives a collection containing the same suggestions in the same order when its call completes. Collection and suggestion object identity across calls is unspecified. The result is an empty collection if no suggestions are available or if [CoreWebView2ContextMenuTarget.HasSpellingError](corewebview2contextmenutarget.md#hasspellingerror) is `false`.
:::code language="csharp" source="../code/sample/SampleApps/WebView2WpfBrowser/MainWindow.xaml.cs" id="SpellCheckSuggestions":::






## Referenced by

- [CoreWebView2ContextMenuRequestedEventArgs](corewebview2contextmenurequestedeventargs.md)
