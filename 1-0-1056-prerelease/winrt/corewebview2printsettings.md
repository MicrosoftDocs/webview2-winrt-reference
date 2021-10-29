---
description: Settings used by the CoreWebView2.PrintToPdfAsync method. Other programmatic printing is not currently supported.
title: CoreWebView2PrintSettings
ms.date: 10/28/2021
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2PrintSettings
---

# CoreWebView2PrintSettings Class



Settings used by the [CoreWebView2.PrintToPdfAsync](corewebview2.md#printtopdfasync) method. Other programmatic printing is not currently supported.

## Summary

Members|Description
--|--
[FooterUri](#footeruri) | The URI in the footer if [CoreWebView2PrintSettings.ShouldPrintHeaderAndFooter](corewebview2printsettings.md#shouldprintheaderandfooter) is `true`.
[HeaderTitle](#headertitle) | The title in the header if [CoreWebView2PrintSettings.ShouldPrintHeaderAndFooter](corewebview2printsettings.md#shouldprintheaderandfooter) is `true`.
[MarginBottom](#marginbottom) | The bottom margin in inches.
[MarginLeft](#marginleft) | The left margin in inches.
[MarginRight](#marginright) | The right margin in inches.
[MarginTop](#margintop) | The top margin in inches.
[Orientation](#orientation) | The orientation can be portrait or landscape.
[PageHeight](#pageheight) | The page height in inches.
[PageWidth](#pagewidth) | The page width in inches.
[ScaleFactor](#scalefactor) | The scale factor is a value between 0.1 and 2.0.
[ShouldPrintBackgrounds](#shouldprintbackgrounds) | `true` if background colors and images should be printed.
[ShouldPrintHeaderAndFooter](#shouldprintheaderandfooter) | `true` if header and footer should be printed.
[ShouldPrintSelectionOnly](#shouldprintselectiononly) | `true` if only the current end user's selection of HTML in the document should be printed.

## Properties

### FooterUri

>  string FooterUri

The URI in the footer if [CoreWebView2PrintSettings.ShouldPrintHeaderAndFooter](corewebview2printsettings.md#shouldprintheaderandfooter) is `true`.
The default value is the current URI. If an empty string or null value is provided, no URI is shown in the footer.

### HeaderTitle

>  string HeaderTitle

The title in the header if [CoreWebView2PrintSettings.ShouldPrintHeaderAndFooter](corewebview2printsettings.md#shouldprintheaderandfooter) is `true`.
The default value is the title of the current document. If an empty string or null value is provided, no title is shown in the header.

### MarginBottom

>  double MarginBottom

The bottom margin in inches.
The default is 1 cm, or ~0.4 inches. A margin cannot be less than zero. The current value is not changed if an invalid value is provided.

### MarginLeft

>  double MarginLeft

The left margin in inches.
The default is 1 cm, or ~0.4 inches. A margin cannot be less than zero. The current value is not changed if an invalid value is provided.

### MarginRight

>  double MarginRight

The right margin in inches.
The default is 1 cm, or ~0.4 inches. A margin cannot be less than zero. The current value is not changed if an invalid value is provided.

### MarginTop

>  double MarginTop

The top margin in inches.
The default is 1 cm, or ~0.4 inches. A margin cannot be less than zero. The current value is not changed if an invalid value is provided.

### Orientation

>  [CoreWebView2PrintOrientation](corewebview2printorientation.md) Orientation

The orientation can be portrait or landscape.
The default orientation is portrait. See [CoreWebView2PrintOrientation](corewebview2printorientation.md).

### PageHeight

>  double PageHeight

The page height in inches.
The default height is 11 inches. The current value is not changed if the provided page width is less than or equal to zero.

### PageWidth

>  double PageWidth

The page width in inches.
The default width is 8.5 inches. The current value is not changed if the provided page width is less than or equal to zero.

### ScaleFactor

>  double ScaleFactor

The scale factor is a value between 0.1 and 2.0.
The default is 1.0. The current value is not changed if an invalid value is provided.

### ShouldPrintBackgrounds

>  bool ShouldPrintBackgrounds

`true` if background colors and images should be printed.
The default value is `false`.

### ShouldPrintHeaderAndFooter

>  bool ShouldPrintHeaderAndFooter

`true` if header and footer should be printed.
The default value is `false`. The header consists of the date and time of printing, and the title of the page. The footer consists of the URI and page number. The height of the header and footer is 0.5 cm, or ~0.2 inches.

### ShouldPrintSelectionOnly

>  bool ShouldPrintSelectionOnly

`true` if only the current end user's selection of HTML in the document should be printed.
The default value is `false`.






## Referenced by

- [CoreWebView2](corewebview2.md)
- [CoreWebView2Environment](corewebview2environment.md)
