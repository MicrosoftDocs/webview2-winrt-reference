---
description: Event args for the CoreWebView2.SaveAsUIShowing event.
title: CoreWebView2SaveAsUIShowingEventArgs
ms.date: 10/17/2024
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2SaveAsUIShowingEventArgs
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- Microsoft.Web.WebView2.Core.CoreWebView2SaveAsUIShowingEventArgs
- Microsoft.Web.WebView2.Core.CoreWebView2SaveAsUIShowingEventArgs.AllowReplace
- Microsoft.Web.WebView2.Core.CoreWebView2SaveAsUIShowingEventArgs.Cancel
- Microsoft.Web.WebView2.Core.CoreWebView2SaveAsUIShowingEventArgs.ContentMimeType
- Microsoft.Web.WebView2.Core.CoreWebView2SaveAsUIShowingEventArgs.Kind
- Microsoft.Web.WebView2.Core.CoreWebView2SaveAsUIShowingEventArgs.SaveAsFilePath
- Microsoft.Web.WebView2.Core.CoreWebView2SaveAsUIShowingEventArgs.SuppressDefaultDialog
- Microsoft.Web.WebView2.Core.CoreWebView2SaveAsUIShowingEventArgs.GetDeferral
- Microsoft.Web.WebView2.Core.CoreWebView2SaveAsUIShowingEventArgs.get_AllowReplace
- Microsoft.Web.WebView2.Core.CoreWebView2SaveAsUIShowingEventArgs.get_Cancel
- Microsoft.Web.WebView2.Core.CoreWebView2SaveAsUIShowingEventArgs.get_ContentMimeType
- Microsoft.Web.WebView2.Core.CoreWebView2SaveAsUIShowingEventArgs.get_Kind
- Microsoft.Web.WebView2.Core.CoreWebView2SaveAsUIShowingEventArgs.get_SaveAsFilePath
- Microsoft.Web.WebView2.Core.CoreWebView2SaveAsUIShowingEventArgs.get_SuppressDefaultDialog
- Microsoft.Web.WebView2.Core.CoreWebView2SaveAsUIShowingEventArgs.put_AllowReplace
- Microsoft.Web.WebView2.Core.CoreWebView2SaveAsUIShowingEventArgs.put_Cancel
- Microsoft.Web.WebView2.Core.CoreWebView2SaveAsUIShowingEventArgs.put_Kind
- Microsoft.Web.WebView2.Core.CoreWebView2SaveAsUIShowingEventArgs.put_SaveAsFilePath
- Microsoft.Web.WebView2.Core.CoreWebView2SaveAsUIShowingEventArgs.put_SuppressDefaultDialog
---

# CoreWebView2SaveAsUIShowingEventArgs Class



Event args for the [CoreWebView2.SaveAsUIShowing](corewebview2.md#saveasuishowing) event.

## Summary

Members|Description
--|--
[AllowReplace](#allowreplace) | Indicates whether to allow replace old file when it already exists in the target save file path.
[Cancel](#cancel) | Indicates whether to cancel the save as before download.
[ContentMimeType](#contentmimetype) | Mime type of content to be saved.
[Kind](#kind) | The option to save content to different document. [CoreWebView2SaveAsKind](corewebview2saveaskind.md)
[SaveAsFilePath](#saveasfilepath) | The absolute full path of save as location.
[SuppressDefaultDialog](#suppressdefaultdialog) | Indicates if the system default dialog will be suppressed.
[GetDeferral](#getdeferral) | Gets a Deferral object.

## Properties

### AllowReplace

>  bool AllowReplace

Indicates whether to allow replace old file when it already exists in the target save file path.
Setting this property to `TRUE` allows existing files to be replaced. Setting this property to `FALSE` will not replace existing files and will return [CoreWebView2SaveAsUIResult.FileAlreadyExists](corewebview2saveasuiresult.md#filealreadyexists).

### Cancel

>  bool Cancel

Indicates whether to cancel the save as before download.
Set this property to `TRUE` to cancel the Save As action and prevent the download from starting. [CoreWebView2.ShowSaveAsUIAsync](corewebview2.md#showsaveasuiasync) returns [CoreWebView2SaveAsUIResult.Cancelled](corewebview2saveasuiresult.md#cancelled).

### ContentMimeType

> readonly  string ContentMimeType

Mime type of content to be saved.

### Kind

>  [CoreWebView2SaveAsKind](corewebview2saveaskind.md) Kind

The option to save content to different document. [CoreWebView2SaveAsKind](corewebview2saveaskind.md)
If it is not allowed for the current document, method [CoreWebView2.ShowSaveAsUIAsync](corewebview2.md#showsaveasuiasync) returns [CoreWebView2SaveAsUIResult.InvalidPath](corewebview2saveasuiresult.md#invalidpath).

### SaveAsFilePath

>  string SaveAsFilePath

The absolute full path of save as location.
It includes the file name and extension. If it is not valid (for example, the root drive does not exist), Save As is denied, and [CoreWebView2SaveAsUIResult.InvalidPath](corewebview2saveasuiresult.md#invalidpath) is returned. If the associated download completes successfully, a target file is saved at this location. If the `Kind` property is [CoreWebView2SaveAsKind.Complete](corewebview2saveaskind.md#complete), there will be an additional directory with resources files.

### SuppressDefaultDialog

>  bool SuppressDefaultDialog

Indicates if the system default dialog will be suppressed.
When this property is FALSE, the default Save As dialog is shown and the values assigned through `SaveAsFilePath`, `AllowReplace` and `Kind` are ignored when the event args invoke completed. When it is `TRUE`, the system dialog is skipped and all assigned values are used.



## Methods

### GetDeferral

> [Deferral](/uwp/api/Windows.Foundation.Deferral) GetDeferral()

Gets a Deferral object.
This will defer showing the default Save As dialog. Use this to Complete the event at a later time to perform a Save As operation.







## Referenced by

- [CoreWebView2](corewebview2.md)
