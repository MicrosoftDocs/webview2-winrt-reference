---
description: Provides methods and properties for finding and navigating through text in the web view.
title: CoreWebView2Find
ms.date: 10/29/2026
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2Find
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2Find
- CoreWebView2Find.ActiveMatchIndex
- CoreWebView2Find.MatchCount
- CoreWebView2Find.FindNext
- CoreWebView2Find.FindPrevious
- CoreWebView2Find.StartAsync
- CoreWebView2Find.Stop
- CoreWebView2Find.ActiveMatchIndexChanged
- CoreWebView2Find.MatchCountChanged
---

# CoreWebView2Find Class



Provides methods and properties for finding and navigating through text in the web view.
This class allows for finding text, navigation between matches, and customization of the find UI.

## Summary

Members|Description
--|--
[ActiveMatchIndex](#activematchindex) | Retrieves the index of the currently active match in the find session.
[MatchCount](#matchcount) | Gets the total count of matches found in the current document based on the last find session's criteria.
[FindNext](#findnext) | Navigates to the next match in the document.
[FindPrevious](#findprevious) | Navigates to the previous match in the document.
[StartAsync](#startasync) | Initiates a find using the specified find options asynchronously.
[Stop](#stop) | Stops the current 'Find' session and hides the Find bar.
[ActiveMatchIndexChanged](#activematchindexchanged) | Raised when the index of the currently active match changes.
[MatchCountChanged](#matchcountchanged) | Raised when the total count of matches in the document changes due to a new find session or changes in the document.

## Properties

### ActiveMatchIndex

> readonly  int ActiveMatchIndex

Retrieves the index of the currently active match in the find session.
Returns the index of the currently active match, or -1 if there is no active match.
The index starts at 1 for the first match.

### MatchCount

> readonly  int MatchCount

Gets the total count of matches found in the current document based on the last find session's criteria.
Returns the total count of matches.



## Methods

### FindNext

> void FindNext()

Navigates to the next match in the document.
If there are no more matches to find, FindNext will wrap around to the first match's index.

If called when there is no find session active, `FindNext` throws an invalid state exception.



### FindPrevious

> void FindPrevious()

Navigates to the previous match in the document.
If there are no more matches to find, FindPrevious will wrap around to the last match's index.

If called when there is no find session active, `FindPrevious` throws an invalid state exception.



### StartAsync

> [IAsyncAction](/uwp/api/Windows.Foundation.IAsyncAction) StartAsync([CoreWebView2FindOptions](corewebview2findoptions.md) options)

Initiates a find using the specified find options asynchronously.
Displays the Find bar and starts the find session. If a find session was already ongoing, it will be stopped and replaced with this new instance.
If [CoreWebView2FindOptions.FindTerm](corewebview2findoptions.md#findterm) is an empty string, the Find bar is displayed but no finding occurs. Changing the [CoreWebView2FindOptions](corewebview2findoptions.md) object after initiation won't affect the ongoing find session.
To change the ongoing find session, [CoreWebView2Find.StartAsync](corewebview2find.md#startasync) must be called again with a new or modified [CoreWebView2FindOptions](corewebview2findoptions.md) object.
[CoreWebView2Find.StartAsync](corewebview2find.md#startasync) supports HTML and TXT document queries. In general, this API is designed for text-based find sessions.
If you start a find session programmatically on another file format that doesn't have text fields, the find session will try to execute but will fail to find any matches. (It will silently fail) Note: The asynchronous action completes when the UI has been displayed with the find term in the UI bar, and the matches have populated on the counter on the find bar.
There may be a slight latency between the UI display and the matches populating in the counter.
The [CoreWebView2Find.MatchCountChanged](corewebview2find.md#matchcountchanged) and [CoreWebView2Find.ActiveMatchIndexChanged](corewebview2find.md#activematchindexchanged) events are only raised after [CoreWebView2Find.StartAsync](corewebview2find.md#startasync) has completed; otherwise, they will have their default values (-1 for active match index and 0 for match count).
To start a new find session (beginning the search from the first match), call [CoreWebView2Find.Stop](corewebview2find.md#stop) before invoking [CoreWebView2Find.StartAsync](corewebview2find.md#startasync).
If [CoreWebView2Find.StartAsync](corewebview2find.md#startasync) is called consecutively with the same options and without calling [CoreWebView2Find.Stop](corewebview2find.md#stop), the find session will continue from the current position in the existing session.
Calling [CoreWebView2Find.StartAsync](corewebview2find.md#startasync) without altering its parameters will behave either as [CoreWebView2Find.FindNext](corewebview2find.md#findnext) or [CoreWebView2Find.FindPrevious](corewebview2find.md#findprevious), depending on the most recent search action performed.
[CoreWebView2Find.StartAsync](corewebview2find.md#startasync) will default to forward if neither have been called.
However, calling [CoreWebView2Find.StartAsync](corewebview2find.md#startasync) again during an ongoing find session does not resume from the point of the current active match. For example, given the text "1 1 A 1 1" and initiating a find session for "A", then starting another find session for "1", it will start searching from the beginning of the document, regardless of the previous active match. This behavior indicates that changing the find query initiates a completely new find session, rather than continuing from the previous match index.



### Stop

> void Stop()

Stops the current 'Find' session and hides the Find bar.
If called with no Find session active, it will silently do nothing.




## Events

### ActiveMatchIndexChanged

Raised when the index of the currently active match changes.
This can happen when the user navigates to a different match or when the active match is changed programmatically.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2Find, Object&gt;

### MatchCountChanged

Raised when the total count of matches in the document changes due to a new find session or changes in the document.

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2Find, Object&gt;



## Referenced by

- [CoreWebView2](corewebview2.md)
