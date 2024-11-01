---
title: CoreWebView2Notification
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/01/2024
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2Notification
---

# runtimeClass CoreWebView2Notification



## Summary

Members|Description
--|--
[BadgeUri](#badgeuri) | 
[Body](#body) | 
[BodyImageUri](#bodyimageuri) | 
[Direction](#direction) | 
[IconUri](#iconuri) | 
[IsSilent](#issilent) | 
[Language](#language) | 
[RequiresInteraction](#requiresinteraction) | 
[ShouldRenotify](#shouldrenotify) | 
[Tag](#tag) | 
[Timestamp](#timestamp) | 
[Title](#title) | 
[VibrationPattern](#vibrationpattern) | 
[ReportClicked](#reportclicked) | 
[ReportClosed](#reportclosed) | 
[ReportShown](#reportshown) | 
[CloseRequested](#closerequested) | 

## Properties

### BadgeUri

> readonly  string BadgeUri

### Body

> readonly  string Body

### BodyImageUri

> readonly  string BodyImageUri

### Direction

> readonly  [CoreWebView2TextDirectionKind](corewebview2textdirectionkind.md) Direction

### IconUri

> readonly  string IconUri

### IsSilent

> readonly  bool IsSilent

### Language

> readonly  string Language

### RequiresInteraction

> readonly  bool RequiresInteraction

### ShouldRenotify

> readonly  bool ShouldRenotify

### Tag

> readonly  string Tag

### Timestamp

> readonly  double Timestamp

### Title

> readonly  string Title

### VibrationPattern

> readonly  [`IVectorView`](/uwp/api/Windows.Foundation.Collections.IVectorView-1)&lt;uint64_t&gt; VibrationPattern



## Methods

### ReportClicked

> void ReportClicked()



### ReportClosed

> void ReportClosed()



### ReportShown

> void ReportShown()




## Events

### CloseRequested

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;[CoreWebView2Notification](corewebview2notification.md), Object&gt;



## Referenced by

- [CoreWebView2NotificationReceivedEventArgs](corewebview2notificationreceivedeventargs.md)
