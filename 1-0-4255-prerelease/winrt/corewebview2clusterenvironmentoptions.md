---
description: The options used to establish or attach to a shared WebView2 cluster environment, identified by a well-known CoreWebView2ClusterEnvironmentOptions.ClusterName that cooperating hosts agree on.
title: CoreWebView2ClusterEnvironmentOptions
ms.date: 09/03/2026
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2ClusterEnvironmentOptions
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- CoreWebView2ClusterEnvironmentOptions
- CoreWebView2ClusterEnvironmentOptions.AdditionalBrowserArguments
- CoreWebView2ClusterEnvironmentOptions.AllowSingleSignOnUsingOSPrimaryAccount
- CoreWebView2ClusterEnvironmentOptions.AreBrowserExtensionsEnabled
- CoreWebView2ClusterEnvironmentOptions.ChannelSearchKind
- CoreWebView2ClusterEnvironmentOptions.ClusterName
- CoreWebView2ClusterEnvironmentOptions.CustomSchemeRegistrations
- CoreWebView2ClusterEnvironmentOptions.EnableTrackingPrevention
- CoreWebView2ClusterEnvironmentOptions.Language
- CoreWebView2ClusterEnvironmentOptions.PerHostProfileIsolation
- CoreWebView2ClusterEnvironmentOptions.ReleaseChannels
---

# CoreWebView2ClusterEnvironmentOptions Class



The options used to establish or attach to a shared WebView2 cluster environment, identified by a well-known [CoreWebView2ClusterEnvironmentOptions.ClusterName](corewebview2clusterenvironmentoptions.md#clustername) that cooperating hosts agree on.
Only options that can be shared process-wide are present. The first host to establish a cluster for a given ClusterName pins these options for as long as the cluster's browser process stays alive; once that browser exits the next host may pin a different set.

## Summary

Members|Description
--|--
[AdditionalBrowserArguments](#additionalbrowserarguments) | Gets or sets additional command-line switches passed to the shared browser process.
[AllowSingleSignOnUsingOSPrimaryAccount](#allowsinglesignonusingosprimaryaccount) | Gets or sets whether single sign on using the OS primary account is allowed for the shared environment. The default is `false`.
[AreBrowserExtensionsEnabled](#arebrowserextensionsenabled) | Gets or sets whether browser extensions are enabled for the shared environment. The default is `false`.
[ChannelSearchKind](#channelsearchkind) | Gets or sets the order that release channels are searched for during shared environment creation.
[ClusterName](#clustername) | Gets or sets the rendezvous name that identifies the cluster.
[CustomSchemeRegistrations](#customschemeregistrations) | A list of custom scheme registrations that are part of the cluster's pinned option set. Hosts that do not request the same registrations get an OptionsMismatch, so this must match the set the cluster was created with in order to join it.
[EnableTrackingPrevention](#enabletrackingprevention) | Gets or sets whether tracking prevention is enabled for the shared environment. The default is `true`.
[Language](#language) | Gets or sets the default display language for the shared environment, in the format of BCP 47 Language Tags.
[PerHostProfileIsolation](#perhostprofileisolation) | Gets or sets whether the effective profile name is namespaced per host application, to prevent accidental cross-app profile use. The default is `true`.
[ReleaseChannels](#releasechannels) | Gets or sets the mask of release channels the shared environment creation searches for.

## Properties

### AdditionalBrowserArguments

>  string AdditionalBrowserArguments

Gets or sets additional command-line switches passed to the shared browser process.
This value is part of the pinned set and is process-wide. See [CoreWebView2EnvironmentOptions.AdditionalBrowserArguments](corewebview2environmentoptions.md#additionalbrowserarguments) for the accepted format and the switches that are ignored.

### AllowSingleSignOnUsingOSPrimaryAccount

>  bool AllowSingleSignOnUsingOSPrimaryAccount

Gets or sets whether single sign on using the OS primary account is allowed for the shared environment. The default is `false`.

### AreBrowserExtensionsEnabled

>  bool AreBrowserExtensionsEnabled

Gets or sets whether browser extensions are enabled for the shared environment. The default is `false`.

### ChannelSearchKind

>  [CoreWebView2ChannelSearchKind](corewebview2channelsearchkind.md) ChannelSearchKind

Gets or sets the order that release channels are searched for during shared environment creation.
Because the browser process is shared, this value is part of the pinned set. The default is [CoreWebView2ChannelSearchKind.MostStable](corewebview2channelsearchkind.md#moststable).


### ClusterName

>  string ClusterName

Gets or sets the rendezvous name that identifies the cluster.
Must be a valid, case-insensitive file-system folder name of at most 64 characters. An invalid value fails the call with `E_INVALIDARG`. To avoid colliding with another application's cluster, include a name you control, such as your company or product name, or a GUID.

### CustomSchemeRegistrations

>  [`IVector`](/uwp/api/Windows.Foundation.Collections.IVector-1)&lt;[CoreWebView2CustomSchemeRegistration](corewebview2customschemeregistration.md)&gt; CustomSchemeRegistrations

A list of custom scheme registrations that are part of the cluster's pinned option set. Hosts that do not request the same registrations get an OptionsMismatch, so this must match the set the cluster was created with in order to join it.

### EnableTrackingPrevention

>  bool EnableTrackingPrevention

Gets or sets whether tracking prevention is enabled for the shared environment. The default is `true`.

### Language

>  string Language

Gets or sets the default display language for the shared environment, in the format of BCP 47 Language Tags.

### PerHostProfileIsolation

>  bool PerHostProfileIsolation

Gets or sets whether the effective profile name is namespaced per host application, to prevent accidental cross-app profile use. The default is `true`.
This is anti-misuse, not a security boundary. It does not encrypt or ACL profile data, and any app that knows the cluster ClusterName and profile name can use a shared profile.

### ReleaseChannels

>  [CoreWebView2ReleaseChannels](corewebview2releasechannels.md) ReleaseChannels

Gets or sets the mask of release channels the shared environment creation searches for.
Because the browser process is shared, this value is part of the pinned set and selects the channel of the shared browser. The default is a mask of all channels. See [CoreWebView2ReleaseChannels](corewebview2releasechannels.md).


## Constructors
### CoreWebView2ClusterEnvironmentOptions

>  CoreWebView2ClusterEnvironmentOptions()







## Referenced by

- [CoreWebView2Environment](corewebview2environment.md)
