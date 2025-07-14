---
description: The result for CoreWebView2.ExecuteScriptWithResultAsync.
title: CoreWebView2ExecuteScriptResult
ms.date: 07/08/2025
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
[Exception](#exception) | If Succeeded is false, you can use this property to get the unhandled exception thrown by script execution
[ResultAsJson](#resultasjson) | A function that has no explicit return value returns undefined. If the script that was run throws an unhandled exception, then the result is also null.
[Succeeded](#succeeded) | This property is true if [CoreWebView2.ExecuteScriptWithResultAsync](corewebview2.md#executescriptwithresultasync) successfully executed script with no unhandled exceptions and the result is available in the [CoreWebView2ExecuteScriptResult.ResultAsJson](corewebview2executescriptresult.md#resultasjson) property.
[TryGetResultAsString](#trygetresultasstring) | If Succeeded is true and the result of script execution is a string, this method provides the value of the string result, and we will get the false var value when the js result is not string type.

## Properties

### Exception

> readonly  [CoreWebView2ScriptException](corewebview2scriptexception.md) Exception

If Succeeded is false, you can use this property to get the unhandled exception thrown by script execution

### ResultAsJson

> readonly  string ResultAsJson

A function that has no explicit return value returns undefined. If the script that was run throws an unhandled exception, then the result is also null.

### Succeeded

> readonly  bool Succeeded

This property is true if [CoreWebView2.ExecuteScriptWithResultAsync](corewebview2.md#executescriptwithresultasync) successfully executed script with no unhandled exceptions and the result is available in the [CoreWebView2ExecuteScriptResult.ResultAsJson](corewebview2executescriptresult.md#resultasjson) property.



## Methods

### TryGetResultAsString

> int TryGetResultAsString(**out** string stringResult)

If Succeeded is true and the result of script execution is a string, this method provides the value of the string result, and we will get the false var value when the js result is not string type.




