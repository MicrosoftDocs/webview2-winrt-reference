---
description: Status of a programmatic Save As call. Indicates the result of the CoreWebView2.ShowSaveAsUIAsync method.
title: CoreWebView2SaveAsUIResult
ms.date: 05/27/2025
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2SaveAsUIResult
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2SaveAsUIResult
---

# CoreWebView2SaveAsUIResult Enum

Status of a programmatic Save As call. Indicates the result of the [CoreWebView2.ShowSaveAsUIAsync](corewebview2.md#showsaveasuiasync) method.

| Name |  Value | Description |
|--|--|--|
|`Success` | 0x0  |  The `ShowSaveAsUIAsync` method call completed successfully. By default, the system Save As dialog opens. If [CoreWebView2SaveAsUIShowingEventArgs.SuppressDefaultDialog](corewebview2saveasuishowingeventargs.md#suppressdefaultdialog) is set to `TRUE`, the system dialog is skipped and the download is started.|
|`InvalidPath` | 0x1  |  Could not perform Save As because the destination file path is an invalid path. The path is invalid when it is empty, a relative path, or a directory, or when the parent path does not exist.|
|`FileAlreadyExists` | 0x2  |  Could not perform Save As because the destination file path already exists and replacing files was not allowed by the [CoreWebView2SaveAsUIShowingEventArgs.AllowReplace](corewebview2saveasuishowingeventargs.md#allowreplace) property.|
|`KindNotSupported` | 0x3  |  Could not perform Save As because the `Kind` property selection is not supported due to content MIME type or system limits. See [CoreWebView2SaveAsKind](corewebview2saveaskind.md) for MIME type limits. System limits include when the `HtmlOnly` kind is selected for an error page at child mode, or when the `Complete` kind is selected and the WebView is running in an App Container.|
|`Cancelled` | 0x4  |  Did not perform Save As because the end user cancelled or the [CoreWebView2SaveAsUIShowingEventArgs.Cancel](corewebview2saveasuishowingeventargs.md#cancel) was set to `TRUE`.|
