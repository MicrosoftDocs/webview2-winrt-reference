---
description: This interface represents a JavaScript exception.
title: CoreWebView2ScriptException
ms.date: 03/13/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ScriptException
---

# CoreWebView2ScriptException Class



This interface represents a JavaScript exception.

## Summary

Members|Description
--|--
[ColumnNumber](#columnnumber) | The column number of the source where the exception occurred. Note that this position starts at 0.
[LineNumber](#linenumber) | The line number of the source where the exception occurred. Note that this position starts at 0.
[Message](#message) | The Message is the exception's message and potentially stack.
[Name](#name) | The Name is the exception's class name.
[ToJson](#tojson) | This will return all details of the exception as a JSON string.

## Properties

### ColumnNumber

> readonly  uint32_t ColumnNumber

The column number of the source where the exception occurred. Note that this position starts at 0.

### LineNumber

> readonly  uint32_t LineNumber

The line number of the source where the exception occurred. Note that this position starts at 0.

### Message

> readonly  string Message

The Message is the exception's message and potentially stack.

### Name

> readonly  string Name

The Name is the exception's class name.

### ToJson

> readonly  string ToJson

This will return all details of the exception as a JSON string.






## Referenced by

- [CoreWebView2ExecuteScriptResult](corewebview2executescriptresult.md)
