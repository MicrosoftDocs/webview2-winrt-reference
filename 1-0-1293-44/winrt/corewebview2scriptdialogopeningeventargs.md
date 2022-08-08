---
description: Event args for the CoreWebView2.ScriptDialogOpening event.
title: CoreWebView2ScriptDialogOpeningEventArgs
ms.date: 08/08/2022
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ScriptDialogOpeningEventArgs
---

# CoreWebView2ScriptDialogOpeningEventArgs Class



Event args for the [CoreWebView2.ScriptDialogOpening](corewebview2.md#scriptdialogopening) event.

## Summary

Members|Description
--|--
[DefaultText](#defaulttext) | Gets the default value to use for the result of the `prompt` JavaScript function.
[Kind](#kind) | Gets the kind of JavaScript dialog box.
[Message](#message) | Gets the message of the dialog box.
[ResultText](#resulttext) | Gets or sets the return value from the JavaScript `prompt` function if [CoreWebView2ScriptDialogOpeningEventArgs.Accept](corewebview2scriptdialogopeningeventargs.md#accept) is run.
[Uri](#uri) | Gets the URI of the page that requested the dialog box.
[Accept](#accept) | Responds with **OK** to `confirm`, `prompt`, and `beforeunload` dialogs. Not run this method to indicate cancel.
[GetDeferral](#getdeferral) | Gets a Deferral object.

## Properties

### DefaultText

> readonly  string DefaultText

Gets the default value to use for the result of the `prompt` JavaScript function.
This is the second parameter passed to the JavaScript prompt dialog.

### Kind

> readonly  [CoreWebView2ScriptDialogKind](corewebview2scriptdialogkind.md) Kind

Gets the kind of JavaScript dialog box.

### Message

> readonly  string Message

Gets the message of the dialog box.
From JavaScript this is the first parameter passed to `alert`, `confirm`, and `prompt` and is empty for `beforeunload`.

### ResultText

>  string ResultText

Gets or sets the return value from the JavaScript `prompt` function if [CoreWebView2ScriptDialogOpeningEventArgs.Accept](corewebview2scriptdialogopeningeventargs.md#accept) is run.
This value is ignored for [CoreWebView2ScriptDialogOpeningEventArgs.Kind](corewebview2scriptdialogopeningeventargs.md#kind)s other than [CoreWebView2ScriptDialogKind](corewebview2scriptdialogkind.md).Prompt. If [CoreWebView2ScriptDialogOpeningEventArgs.Accept](corewebview2scriptdialogopeningeventargs.md#accept) is not run, this value is ignored and `false` is returned from `prompt`.

### Uri

> readonly  string Uri

Gets the URI of the page that requested the dialog box.



## Methods

### Accept

> void Accept()

Responds with **OK** to `confirm`, `prompt`, and `beforeunload` dialogs. Not run this method to indicate cancel.
From JavaScript, this means that the `confirm` function and `beforeunload` event returns `true` if Accept is run. And for the `prompt` function it returns the value of [CoreWebView2ScriptDialogOpeningEventArgs.ResultText](corewebview2scriptdialogopeningeventargs.md#resulttext) if Accept is run and otherwise returns `false`.



### GetDeferral

> [Deferral](/uwp/api/Windows.Foundation.Deferral) GetDeferral()

Gets a Deferral object.
Use this to Complete the event at a later time.






## Referenced by

- [CoreWebView2](corewebview2.md)
