---
description: Represents a spelling correction for the current context menu target.
title: CoreWebView2SpellCheckSuggestion
ms.date: 10/28/2026
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2SpellCheckSuggestion
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2SpellCheckSuggestion
- CoreWebView2SpellCheckSuggestion.CommandId
- CoreWebView2SpellCheckSuggestion.SuggestionText
---

# CoreWebView2SpellCheckSuggestion Class



Represents a spelling correction for the current context menu target.
This object remains readable while retained. Its [CoreWebView2SpellCheckSuggestion.CommandId](corewebview2spellchecksuggestion.md#commandid) is valid only for the originating context menu request and must be assigned before that request's deferral is completed.

## Summary

Members|Description
--|--
[CommandId](#commandid) | Gets the opaque command ID used to apply this correction.
[SuggestionText](#suggestiontext) | Gets the browser-generated spelling correction text.

## Properties

### CommandId

> readonly  int CommandId

Gets the opaque command ID used to apply this correction.
Assign this value to [CoreWebView2ContextMenuRequestedEventArgs.SelectedCommandId](corewebview2contextmenurequestedeventargs.md#selectedcommandid) before completing the context menu deferral. Do not invent, modify, or retain this value for a later context menu request.

### SuggestionText

> readonly  string SuggestionText

Gets the browser-generated spelling correction text.




