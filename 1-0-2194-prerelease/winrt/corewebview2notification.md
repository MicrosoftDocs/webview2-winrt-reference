---
description: 
title: CoreWebView2Notification
ms.date: 11/06/2023
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2Notification
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- Microsoft.Web.WebView2.Core.CoreWebView2Notification
- Microsoft.Web.WebView2.Core.CoreWebView2Notification.BadgeUri
- Microsoft.Web.WebView2.Core.CoreWebView2Notification.Body
- Microsoft.Web.WebView2.Core.CoreWebView2Notification.BodyImageUri
- Microsoft.Web.WebView2.Core.CoreWebView2Notification.Direction
- Microsoft.Web.WebView2.Core.CoreWebView2Notification.IconUri
- Microsoft.Web.WebView2.Core.CoreWebView2Notification.IsSilent
- Microsoft.Web.WebView2.Core.CoreWebView2Notification.Language
- Microsoft.Web.WebView2.Core.CoreWebView2Notification.RequiresInteraction
- Microsoft.Web.WebView2.Core.CoreWebView2Notification.ShouldRenotify
- Microsoft.Web.WebView2.Core.CoreWebView2Notification.Tag
- Microsoft.Web.WebView2.Core.CoreWebView2Notification.Timestamp
- Microsoft.Web.WebView2.Core.CoreWebView2Notification.Title
- Microsoft.Web.WebView2.Core.CoreWebView2Notification.ReportClicked
- Microsoft.Web.WebView2.Core.CoreWebView2Notification.ReportClosed
- Microsoft.Web.WebView2.Core.CoreWebView2Notification.ReportShown
- Microsoft.Web.WebView2.Core.CoreWebView2Notification.add_CloseRequested
- Microsoft.Web.WebView2.Core.CoreWebView2Notification.get_BadgeUri
- Microsoft.Web.WebView2.Core.CoreWebView2Notification.get_Body
- Microsoft.Web.WebView2.Core.CoreWebView2Notification.get_BodyImageUri
- Microsoft.Web.WebView2.Core.CoreWebView2Notification.get_Direction
- Microsoft.Web.WebView2.Core.CoreWebView2Notification.get_IconUri
- Microsoft.Web.WebView2.Core.CoreWebView2Notification.get_IsSilent
- Microsoft.Web.WebView2.Core.CoreWebView2Notification.get_Language
- Microsoft.Web.WebView2.Core.CoreWebView2Notification.get_RequiresInteraction
- Microsoft.Web.WebView2.Core.CoreWebView2Notification.get_ShouldRenotify
- Microsoft.Web.WebView2.Core.CoreWebView2Notification.get_Tag
- Microsoft.Web.WebView2.Core.CoreWebView2Notification.get_Timestamp
- Microsoft.Web.WebView2.Core.CoreWebView2Notification.get_Title
- Microsoft.Web.WebView2.Core.CoreWebView2Notification.remove_CloseRequested
- Microsoft.Web.WebView2.Core.CoreWebView2Notification.CloseRequested
---

# CoreWebView2Notification Class



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



## Methods

### ReportClicked

> void ReportClicked()



### ReportClosed

> void ReportClosed()



### ReportShown

> void ReportShown()




## Events

### CloseRequested

Type: [TypedEventHandler](/uwp/api/Windows.Foundation.TypedEventHandler-2)&lt;CoreWebView2Notification, Object&gt;



## Referenced by

- [CoreWebView2NotificationReceivedEventArgs](corewebview2notificationreceivedeventargs.md)
