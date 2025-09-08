---
description: Provides methods and properties for finding and navigating through text in the web view. This interface allows for finding text, navigation between matches, and customization of the find UI.
title: CoreWebView2Find
ms.date: 09/01/2025
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



Provides methods and properties for finding and navigating through text in the web view. This interface allows for finding text, navigation between matches, and customization of the find UI.


## Summary

Members|Description
--|--
[ActiveMatchIndex](#activematchindex) | Retrieves the index of the currently active match in the find session. Returns the index of the currently active match, or -1 if there is no active match.
[MatchCount](#matchcount) | Gets the total count of matches found in the current document based on the last find session's criteria.
[FindNext](#findnext) | Navigates to the next match in the document.
[FindPrevious](#findprevious) | Navigates to the previous match in the document.
[StartAsync](#startasync) | Initiates a find using the specified find options asynchronously.
[Stop](#stop) | Stops the current 'Find' session and hides the Find bar.
[ActiveMatchIndexChanged](#activematchindexchanged) | Registers an event handler for the ActiveMatchIndexChanged event. This event is raised when the index of the currently active match changes.
[MatchCountChanged](#matchcountchanged) | Registers an event handler for the MatchCountChanged event. This event is raised when the total count of matches in the document changes due to a new find session or changes in the document.

## Properties

### ActiveMatchIndex

> readonly  int ActiveMatchIndex

Retrieves the index of the currently active match in the find session. Returns the index of the currently active match, or -1 if there is no active match.
The index starts at 1 for the first match.


### MatchCount

> readonly  int MatchCount

Gets the total count of matches found in the current document based on the last find session's criteria.
The total count of matches.




## Methods

### FindNext

> void FindNext()

Navigates to the next match in the document.
 If there are no matches to find, FindNext will wrap around to the first match's index. If called when there is no find session active, FindNext will silently fail. 




### FindPrevious

> void FindPrevious()

Navigates to the previous match in the document.
If there are no matches to find, FindPrevious will wrap around to the last match's index. If called when there is no find session active, FindPrevious will silently fail.




### StartAsync

> [IAsyncAction](/uwp/api/Windows.Foundation.IAsyncAction) StartAsync([CoreWebView2FindOptions](corewebview2findoptions.md) options)

Initiates a find operation using the specified options asynchronously. Starting find is an asynchronous operation and can be configured with notification handlers to know when the starting find operation has completed. The Find dialog will appear after the StartAsync operation completes. Note that the async behavior only applies to starting the find, not to the entire find dialog session.

Displays the Find bar and starts the find session, replacing any existing session. Shows the Find bar even with empty search strings (no actual finding occurs). Supports HTML and TXT document queries; silently fails on unsupported formats. FindOptions changes after initiation don't affect the active session.

The async action completes when the Find bar UI displays the search term and the match counter populates (may have slight latency). The `MatchCountChanged` and `ActiveMatchIndexChanged` events fire only after completion with default values of -1 for active match index and 0 for match count before completion.

To start a new session from the first match, call `Stop()` before `StartAsync()`. Consecutive calls with the same options continue from the current position. Without parameters, it behaves as `FindNext` or `FindPrevious` based on the last action (defaults to forward). Different search terms always start a new session from the document beginning.




### Stop

> void Stop()

Stops the current 'Find' session and hides the Find bar. Stopping Find is an asynchronous operation and can be configured with notification handlers to know when stopping find operation has completed. The Find dialog will disappear before the Stop operation completes. If called with no Find session active, it will silently do nothing.





## Events

### ActiveMatchIndexChanged

Registers an event handler for the ActiveMatchIndexChanged event. This event is raised when the index of the currently active match changes.


Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2Find, Object&gt;

### MatchCountChanged

Registers an event handler for the MatchCountChanged event. This event is raised when the total count of matches in the document changes due to a new find session or changes in the document.


Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2Find, Object&gt;



## Referenced by

- [CoreWebView2](corewebview2.md)
