---
description: Provides crash signature data captured at the moment of process failure.
title: CoreWebView2CrashReport
ms.date: 06/30/2026
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2CrashReport
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2CrashReport
- CoreWebView2CrashReport.BucketId
- CoreWebView2CrashReport.CrashReportId
- CoreWebView2CrashReport.ExceptionCode
- CoreWebView2CrashReport.FaultOffset
- CoreWebView2CrashReport.FaultingModuleName
- CoreWebView2CrashReport.FaultingModuleVersion
- CoreWebView2CrashReport.ReportTime
---

# CoreWebView2CrashReport Class



Provides crash signature data captured at the moment of process failure.
`CrashReport` is `null` when the failure did not produce a crash report (normal exit, external kill, launch failure, hang). Host apps should always check for `null` before accessing properties.

## Summary

Members|Description
--|--
[BucketId](#bucketid) | Crash bucket identifier assigned by Microsoft's crash telemetry service. Returned as a 32-character hex string. Empty when no bucket was assigned: crash data was not uploaded to Microsoft's telemetry service (custom crash reporting enabled), or no response was received from the telemetry service (network throttled or unavailable).
[CrashReportId](#crashreportid) | The unique identifier (UUID) for this crash report. Use this to locate the corresponding dump file in `FailureReportFolderPath`.
[ExceptionCode](#exceptioncode) | The Windows exception code for the failure, e.g. `0xC0000005` for `STATUS_ACCESS_VIOLATION`. `0` if not available.
[FaultOffset](#faultoffset) | Relative virtual address (RVA) of the faulting instruction within `FaultingModuleName`. `0` if not available.
[FaultingModuleName](#faultingmodulename) | Basename of the module containing the faulting instruction, e.g. `renderer.dll`.
[FaultingModuleVersion](#faultingmoduleversion) | Version of the faulting module, e.g. `128.0.2739.42`.
[ReportTime](#reporttime) | Time the crash report was recorded, as a Windows FILETIME value (100-nanosecond intervals since Jan 1 1601 UTC). `0` if unavailable.

## Properties

### BucketId

> readonly  string BucketId

Crash bucket identifier assigned by Microsoft's crash telemetry service. Returned as a 32-character hex string. Empty when no bucket was assigned: crash data was not uploaded to Microsoft's telemetry service (custom crash reporting enabled), or no response was received from the telemetry service (network throttled or unavailable).

### CrashReportId

> readonly  string CrashReportId

The unique identifier (UUID) for this crash report. Use this to locate the corresponding dump file in `FailureReportFolderPath`.

### ExceptionCode

> readonly  uint32_t ExceptionCode

The Windows exception code for the failure, e.g. `0xC0000005` for `STATUS_ACCESS_VIOLATION`. `0` if not available.

### FaultOffset

> readonly  uint64_t FaultOffset

Relative virtual address (RVA) of the faulting instruction within `FaultingModuleName`. `0` if not available.

### FaultingModuleName

> readonly  string FaultingModuleName

Basename of the module containing the faulting instruction, e.g. `renderer.dll`.

### FaultingModuleVersion

> readonly  string FaultingModuleVersion

Version of the faulting module, e.g. `128.0.2739.42`.

### ReportTime

> readonly  uint64_t ReportTime

Time the crash report was recorded, as a Windows FILETIME value (100-nanosecond intervals since Jan 1 1601 UTC). `0` if unavailable.






## Referenced by

- [CoreWebView2ProcessFailedEventArgs](corewebview2processfailedeventargs.md)
