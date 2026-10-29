---
description: Event args for the CoreWebView2.SaveAsUIShowing event.
title: CoreWebView2SaveAsUIShowingEventArgs
ms.date: 10-29-2026
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2SaveAsUIShowingEventArgs
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2SaveAsUIShowingEventArgs
- CoreWebView2SaveAsUIShowingEventArgs.AllowReplace
- CoreWebView2SaveAsUIShowingEventArgs.Cancel
- CoreWebView2SaveAsUIShowingEventArgs.ContentMimeType
- CoreWebView2SaveAsUIShowingEventArgs.Kind
- CoreWebView2SaveAsUIShowingEventArgs.SaveAsFilePath
- CoreWebView2SaveAsUIShowingEventArgs.SuppressDefaultDialog
- CoreWebView2SaveAsUIShowingEventArgs.GetDeferral
---

# CoreWebView2SaveAsUIShowingEventArgs Class



Event args for the [CoreWebView2.SaveAsUIShowing](corewebview2.md#saveasuishowing) event.

## Summary

Members|Description
--|--
[AllowReplace](#allowreplace) | Indicates whether to allow replacing an existing file at the target save file path.
[Cancel](#cancel) | Indicates whether to cancel the Save As action before download.
[ContentMimeType](#contentmimetype) | Mime type of content to be saved.
[Kind](#kind) | The option to save content as a different document kind.
[SaveAsFilePath](#saveasfilepath) | The absolute full path of the Save As location.
[SuppressDefaultDialog](#suppressdefaultdialog) | Indicates if the system default dialog will be suppressed.
[GetDeferral](#getdeferral) | Gets a [Deferral](/uwp/api/windows.foundation.deferral) object.

## Properties

### AllowReplace

>  bool AllowReplace

Indicates whether to allow replacing an existing file at the target save file path.

Setting this property to `true` allows existing files to be replaced. Setting this property to `false` will not replace existing files and will return [CoreWebView2SaveAsUIResult](corewebview2saveasuiresult.md).FileAlreadyExists.

### Cancel

>  bool Cancel

Indicates whether to cancel the Save As action before download.

Set this property to `true` to cancel the Save As action and prevent the download from starting. [CoreWebView2.ShowSaveAsUIAsync](corewebview2.md#showsaveasuiasync) returns [CoreWebView2SaveAsUIResult](corewebview2saveasuiresult.md).Cancelled.

### ContentMimeType

> readonly  string ContentMimeType

Mime type of content to be saved.

### Kind

>  [CoreWebView2SaveAsKind](corewebview2saveaskind.md) Kind

The option to save content as a different document kind.
See [CoreWebView2SaveAsKind](corewebview2saveaskind.md).

If it is not allowed for the current document, [CoreWebView2.ShowSaveAsUIAsync](corewebview2.md#showsaveasuiasync) returns [CoreWebView2SaveAsUIResult](corewebview2saveasuiresult.md).KindNotSupported.

### SaveAsFilePath

>  string SaveAsFilePath

The absolute full path of the Save As location.

It includes the file name and extension. If it is not valid (for example, the root drive does not exist), Save As is denied, and [CoreWebView2SaveAsUIResult](corewebview2saveasuiresult.md).InvalidPath is returned. If the associated download completes successfully, a target file is saved at this location. If the [CoreWebView2SaveAsUIShowingEventArgs.Kind](corewebview2saveasuishowingeventargs.md#kind) property is [CoreWebView2SaveAsKind](corewebview2saveaskind.md).Complete, there will be an additional directory with resource files.

### SuppressDefaultDialog

>  bool SuppressDefaultDialog

Indicates if the system default dialog will be suppressed.

When this property is `false`, the default Save As dialog is shown and the values assigned through [CoreWebView2SaveAsUIShowingEventArgs.SaveAsFilePath](corewebview2saveasuishowingeventargs.md#saveasfilepath), [CoreWebView2SaveAsUIShowingEventArgs.AllowReplace](corewebview2saveasuishowingeventargs.md#allowreplace), and [CoreWebView2SaveAsUIShowingEventArgs.Kind](corewebview2saveasuishowingeventargs.md#kind) are ignored when the event handler completes. When it is `true`, the system dialog is skipped and all assigned values are used.



## Methods

### GetDeferral

> [Deferral](/uwp/api/Windows.Foundation.Deferral) GetDeferral()

Gets a [Deferral](/uwp/api/windows.foundation.deferral) object.

This will defer showing the default Save As dialog. Use this to [Deferral.Complete](/uwp/api/windows.foundation.deferral.complete) the event at a later time to perform a Save As operation.






## Referenced by

- [CoreWebView2](corewebview2.md)
