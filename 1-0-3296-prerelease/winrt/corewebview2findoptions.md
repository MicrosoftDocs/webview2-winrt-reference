---
description: Defines the options for a find session in the WebView2 control. This interface provides the necessary properties to configure a find session
title: CoreWebView2FindOptions
ms.date: 05/06/2025
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2FindOptions
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2FindOptions
- CoreWebView2FindOptions.FindTerm
- CoreWebView2FindOptions.IsCaseSensitive
- CoreWebView2FindOptions.ShouldHighlightAllMatches
- CoreWebView2FindOptions.ShouldMatchWord
- CoreWebView2FindOptions.SuppressDefaultFindDialog
---

# CoreWebView2FindOptions Class



Defines the options for a find session in the WebView2 control. This interface provides the necessary properties to configure a find session


## Summary

Members|Description
--|--
[FindTerm](#findterm) | Gets or sets the word or phrase to be searched in the current page.
[IsCaseSensitive](#iscasesensitive) | Gets or sets a value indicating whether the find session is case sensitive
[ShouldHighlightAllMatches](#shouldhighlightallmatches) | Gets or sets a value indicating whether all matches should be highlighted
[ShouldMatchWord](#shouldmatchword) | Gets or sets a value indicating whether only whole words should be matched during the find session.
[SuppressDefaultFindDialog](#suppressdefaultfinddialog) | Gets or sets a value indicating whether the default Find UI should be suppressed.

## Properties

### FindTerm

>  string FindTerm

Gets or sets the word or phrase to be searched in the current page.
You can set FindTerm to any text you want to find on the page. This will take effect the next time you call the Start method. 


### IsCaseSensitive

>  bool IsCaseSensitive

Gets or sets a value indicating whether the find session is case sensitive
When toggling case sensitivity, the behavior can vary by locale, which may be influenced by both the browser's UI locale and the document's language settings. The browser's UI locale typically provides a default handling approach, while the document's language settings (e.g., specified using the HTML lang attribute) can override these defaults to apply locale-specific rules. This dual consideration ensures that text is processed in a manner consistent with user expectations and the linguistic context of the content. 


### ShouldHighlightAllMatches

>  bool ShouldHighlightAllMatches

Gets or sets a value indicating whether all matches should be highlighted
 Returns true< if all matches are highlighted, false otherwise. Note: Changes to this property take effect only when Start, FindNext, or FindPrevious is called. Preferences for the session cannot be updated unless another call to the Start function on the server-side is made. Therefore, changes will not take effect until one of these functions is called.


### ShouldMatchWord

>  bool ShouldMatchWord

Gets or sets a value indicating whether only whole words should be matched during the find session.
 Similar to case sensitivity, word matching also can vary by locale, which may be influenced by both the browser's UI locale and the document's language settings. The browser's UI locale typically provides a default handling approach, while the document's language settings (e.g., specified using the HTML lang attribute) can override these defaults to apply locale-specific rules. This dual consideration ensures that text is processed in a manner consistent with user expectations and the linguistic context of the content.


### SuppressDefaultFindDialog

>  bool SuppressDefaultFindDialog

Gets or sets a value indicating whether the default Find UI should be suppressed.
 You can use this to hide the default UI so that you can show your own custom UI or programmatically interact with the Find API while showing no Find UI. Returns true if hiding the default Find UI and false if showing the default Find UI. Note: Changes to this property take effect only when Start, FindNext, or FindPrevious is called. Preferences for the session cannot be updated unless another call to the Start function on the server-side is made. Therefore, changes will not take effect until one of these functions is called. 






## Referenced by

- [CoreWebView2Environment](corewebview2environment.md)
- [CoreWebView2Find](corewebview2find.md)
