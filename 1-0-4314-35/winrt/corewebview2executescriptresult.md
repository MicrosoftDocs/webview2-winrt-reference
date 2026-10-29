---
description: The result for CoreWebView2.ExecuteScriptWithResultAsync.
title: CoreWebView2ExecuteScriptResult
ms.date: 10-29-2026
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ExecuteScriptResult
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2ExecuteScriptResult
- CoreWebView2ExecuteScriptResult.Exception
- CoreWebView2ExecuteScriptResult.ResultAsJson
- CoreWebView2ExecuteScriptResult.Succeeded
- CoreWebView2ExecuteScriptResult.TryGetResultAsString
---

# CoreWebView2ExecuteScriptResult Class



The result for [CoreWebView2.ExecuteScriptWithResultAsync](corewebview2.md#executescriptwithresultasync).

## Summary

Members|Description
--|--
[Exception](#exception) | Gets the unhandled exception thrown by script execution when [CoreWebView2ExecuteScriptResult.Succeeded](corewebview2executescriptresult.md#succeeded) is `false`.
[ResultAsJson](#resultasjson) | Gets the JSON encoded string that represents the result of running the provided JavaScript.
[Succeeded](#succeeded) | This property is true if [CoreWebView2.ExecuteScriptWithResultAsync](corewebview2.md#executescriptwithresultasync) successfully executed script with no unhandled exceptions and the result is available in the [CoreWebView2ExecuteScriptResult.ResultAsJson](corewebview2executescriptresult.md#resultasjson) property.
[TryGetResultAsString](#trygetresultasstring) | If [CoreWebView2ExecuteScriptResult.Succeeded](corewebview2executescriptresult.md#succeeded) is `true` and the result of script execution is a string, this method provides the value of the string result, and returns 0 when the JavaScript result is not a string type.

## Properties

### Exception

> readonly  [CoreWebView2ScriptException](corewebview2scriptexception.md) Exception

Gets the unhandled exception thrown by script execution when [CoreWebView2ExecuteScriptResult.Succeeded](corewebview2executescriptresult.md#succeeded) is `false`.

If [CoreWebView2ExecuteScriptResult.Succeeded](corewebview2executescriptresult.md#succeeded) is `true`, accessing this property throws an invalid argument exception.

### ResultAsJson

> readonly  string ResultAsJson

Gets the JSON encoded string that represents the result of running the provided JavaScript.

If the result is `undefined`, contains a reference cycle, or otherwise is not able to be encoded into JSON, then the result is considered to be `null`, which is encoded in JSON as the string `"null"`. A function that has no explicit return value returns `undefined`. If the script that was run throws an unhandled exception, then the result is also `"null"`.

### Succeeded

> readonly  bool Succeeded

This property is true if [CoreWebView2.ExecuteScriptWithResultAsync](corewebview2.md#executescriptwithresultasync) successfully executed script with no unhandled exceptions and the result is available in the [CoreWebView2ExecuteScriptResult.ResultAsJson](corewebview2executescriptresult.md#resultasjson) property.



## Methods

### TryGetResultAsString

> int TryGetResultAsString(**out** string stringResult)

If [CoreWebView2ExecuteScriptResult.Succeeded](corewebview2executescriptresult.md#succeeded) is `true` and the result of script execution is a string, this method provides the value of the string result, and returns 0 when the JavaScript result is not a string type.




