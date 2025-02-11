---
description: Provides methods and properties for finding and navigating through text in the web view. This interface allows for finding text, navigation between matches, and customization of the find UI.
title: CoreWebView2Find
ms.date: 02/04/2025
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

Initiates a find using the specified find options asynchronously.
Displays the Find bar and starts the find session. If a find session was already ongoing, it will be stopped and replaced with this new instance.
If called with an empty string, the Find bar is displayed but no finding occurs. Changing the FindOptions object after initiation won't affect the ongoing find session.
To change the ongoing find session, Start must be called again with a new or modified FindOptions object.
Start supports HTML and TXT document queries. In general, this API is designed for text-based find sessions.
If you start a find session programmatically on another file format that doesn't have text fields, the find session will try to execute but will fail to find any matches. (It will silently fail)
Note: The asynchronous action completes when the UI has been displayed with the find term in the UI bar, and the matches have populated on the counter on the find bar.
There may be a slight latency between the UI display and the matches populating in the counter.
The MatchCountChanged and ActiveMatchIndexChanged events are only raised after Start has completed; otherwise, they will have their default values (-1 for active match index and 0 for match count).
To start a new find session (beginning the search from the first match), call Stop before invoking Start.
If Start is called consecutively with the same options and without calling Stop, the find session
will continue from the current position in the existing session.
Calling Start without altering its parameters will behave either as FindNext or FindPrevious, depending on the most recent search action performed.
Start will default to forward if neither have been called.
However, calling Start again during an ongoing find session does not resume from the point
of the current active match. For example, given the text "1 1 A 1 1" and initiating a find session for "A",
then starting another find session for "1", it will start searching from the beginning of the document,
regardless of the previous active match. This behavior indicates that changing the find query initiates a
completely new find session, rather than continuing from the previous match index.




### Stop

> void Stop()

Stops the current 'Find' session and hides the Find bar.
If called with no Find session active, it will silently do nothing.





## Events

### ActiveMatchIndexChanged

Registers an event handler for the ActiveMatchIndexChanged event. This event is raised when the index of the currently active match changes.


Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2Find, Object&gt;

### MatchCountChanged

Registers an event handler for the MatchCountChanged event. This event is raised when the total count of matches in the document changes due to a new find session or changes in the document.


Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2Find, Object&gt;



## Referenced by

- [CoreWebView2](corewebview2.md)
