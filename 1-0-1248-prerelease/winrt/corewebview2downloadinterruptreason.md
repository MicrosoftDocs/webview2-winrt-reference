---
description: The reason why the CoreWebView2DownloadOperation was interrupted.
title: CoreWebView2DownloadInterruptReason
ms.date: 05/17/2022
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2DownloadInterruptReason
---

# CoreWebView2DownloadInterruptReason Enum

The reason why the [CoreWebView2DownloadOperation](corewebview2downloadoperation.md) was interrupted.

| Name |  Value | Description |
|--|--|--|
|`None` | 0x0  |  No interrupt reason.|
|`FileFailed` | 0x1  |  Generic file error.|
|`FileAccessDenied` | 0x2  |  Access denied due to security restrictions.|
|`FileNoSpace` | 0x3  |  Disk full. User should free some space or choose a different location to store the file.|
|`FileNameTooLong` | 0x4  |  Result file path with file name is too long.|
|`FileTooLarge` | 0x5  |  File is too large for file system.|
|`FileMalicious` | 0x6  |  Microsoft Defender Smartscreen detected a virus in the file.|
|`FileTransientError` | 0x7  |  File was in use, too many files opened, or out of memory.|
|`FileBlockedByPolicy` | 0x8  |  File blocked by local policy.|
|`FileSecurityCheckFailed` | 0x9  |  Security check failed unexpectedly. Microsoft Defender SmartScreen could not scan this file.|
|`FileTooShort` | 0xa  |  Seeking past the end of a file in opening a file, as part of resuming an interrupted download. The file did not exist or was not as large as expected. Partially downloaded file was truncated or deleted, and download will be restarted automatically.|
|`FileHashMismatch` | 0xb  |  Partial file did not match the expected hash and was deleted. Download will be restarted automatically.|
|`NetworkFailed` | 0xc  |  Generic network error. User can retry the download manually.|
|`NetworkTimeout` | 0xd  |  Network operation timed out.|
|`NetworkDisconnected` | 0xe  |  Network connection lost. User can retry the download manually.|
|`NetworkServerDown` | 0xf  |  Server has gone down. User can retry the download manually.|
|`NetworkInvalidRequest` | 0x10  |  Network request invalid because original or redirected URI is invalid, has an unsupported scheme, or is disallowed by network policy.|
|`ServerFailed` | 0x11  |  Generic server error. User can retry the download manually.|
|`ServerNoRange` | 0x12  |  Server does not support range requests.|
|`ServerBadContent` | 0x13  |  Server does not have the requested data.|
|`ServerUnauthorized` | 0x14  |  Server did not authorize access to resource.|
|`ServerCertificateProblem` | 0x15  |  Server certificate problem.|
|`ServerForbidden` | 0x16  |  Server access forbidden.|
|`ServerUnexpectedResponse` | 0x17  |  Unexpected server response. Responding server may not be intended server. User can retry the download manually.|
|`ServerContentLengthMismatch` | 0x18  |  Server sent fewer bytes than the Content-Length header. Content-Length header may be invalid or connection may have closed. Download is treated as complete unless there are [strong validators](https://tools.ietf.org/html/rfc7232#section-2) present to interrupt the download.|
|`ServerCrossOriginRedirect` | 0x19  |  Unexpected cross-origin redirect.|
|`UserCanceled` | 0x1a  |  User canceled the download.|
|`UserShutdown` | 0x1b  |  User shut down the WebView. Resuming downloads that were interrupted during shutdown is not yet supported.|
|`UserPaused` | 0x1c  |  User paused the download.|
|`DownloadProcessCrashed` | 0x1d  |  WebView crashed.|


## Referenced by

- [CoreWebView2DownloadOperation](corewebview2downloadoperation.md)
