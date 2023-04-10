---
description: The result for CoreWebView2.ExecuteScriptWithResultAsync.
title: CoreWebView2ExecuteScriptResult
ms.date: 04/10/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ExecuteScriptResult
---

# CoreWebView2ExecuteScriptResult Class



The result for [CoreWebView2.ExecuteScriptWithResultAsync](corewebview2.md#executescriptwithresultasync).

## Summary

Members|Description
--|--
[Exception](#exception) | If Succeeded is false, you can use this property to get the unhandled exception thrown by script execution
[ResultAsJson](#resultasjson) | A function that has no explicit return value returns undefined. If the script that was run throws an unhandled exception, then the result is also null.
[Succeeded](#succeeded) | This property is true if [CoreWebView2.ExecuteScriptWithResultAsync](corewebview2.md#executescriptwithresultasync) successfully executed script with no unhandled exceptions and the result is available in the [CoreWebView2ExecuteScriptResult.ResultAsJson](corewebview2executescriptresult.md#resultasjson) property.

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




