---
description: Settings used by the CoreWebView2.PrintToPdfAsync method.
title: CoreWebView2PrintSettings
ms.date: 05/20/2024
keywords: webview2, webview, winrt, win32, edge, CoreWebView2, CoreWebView2Controller, browser control, edge html, CoreWebView2PrintSettings
topic_type:
- APIRef
api_type:
- Assembly
api_location:
- Microsoft.Web.WebView2.Core.dll
api_name:
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.Collation
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.ColorMode
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.Copies
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.Duplex
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.FooterUri
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.HeaderTitle
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.MarginBottom
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.MarginLeft
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.MarginRight
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.MarginTop
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.MediaSize
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.Orientation
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.PageHeight
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.PageRanges
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.PageWidth
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.PagesPerSide
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.PrinterName
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.ScaleFactor
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.ShouldPrintBackgrounds
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.ShouldPrintHeaderAndFooter
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.ShouldPrintSelectionOnly
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.get_Collation
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.get_ColorMode
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.get_Copies
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.get_Duplex
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.get_FooterUri
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.get_HeaderTitle
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.get_MarginBottom
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.get_MarginLeft
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.get_MarginRight
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.get_MarginTop
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.get_MediaSize
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.get_Orientation
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.get_PageHeight
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.get_PageRanges
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.get_PageWidth
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.get_PagesPerSide
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.get_PrinterName
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.get_ScaleFactor
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.get_ShouldPrintBackgrounds
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.get_ShouldPrintHeaderAndFooter
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.get_ShouldPrintSelectionOnly
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.put_Collation
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.put_ColorMode
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.put_Copies
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.put_Duplex
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.put_FooterUri
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.put_HeaderTitle
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.put_MarginBottom
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.put_MarginLeft
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.put_MarginRight
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.put_MarginTop
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.put_MediaSize
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.put_Orientation
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.put_PageHeight
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.put_PageRanges
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.put_PageWidth
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.put_PagesPerSide
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.put_PrinterName
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.put_ScaleFactor
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.put_ShouldPrintBackgrounds
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.put_ShouldPrintHeaderAndFooter
- Microsoft.Web.WebView2.Core.CoreWebView2PrintSettings.put_ShouldPrintSelectionOnly
---

# CoreWebView2PrintSettings Class



Settings used by the [CoreWebView2.PrintToPdfAsync](corewebview2.md#printtopdfasync) method.

## Summary

Members|Description
--|--
[Collation](#collation) | Printer collation.
[ColorMode](#colormode) | Printer color mode.
[Copies](#copies) | Number of copies to print. Minimum value is `1` and the maximum copies count is `999`.
[Duplex](#duplex) | Printer duplex settings.
[FooterUri](#footeruri) | The URI in the footer if [CoreWebView2PrintSettings.ShouldPrintHeaderAndFooter](corewebview2printsettings.md#shouldprintheaderandfooter) is `true`.
[HeaderTitle](#headertitle) | The title in the header if [CoreWebView2PrintSettings.ShouldPrintHeaderAndFooter](corewebview2printsettings.md#shouldprintheaderandfooter) is `true`.
[MarginBottom](#marginbottom) | The bottom margin in inches.
[MarginLeft](#marginleft) | The left margin in inches.
[MarginRight](#marginright) | The right margin in inches.
[MarginTop](#margintop) | The top margin in inches.
[MediaSize](#mediasize) | Printer media size.
[Orientation](#orientation) | The orientation can be portrait or landscape.
[PageHeight](#pageheight) | The page height in inches.
[PageRanges](#pageranges) | Page range to print. Defaults to empty string, which means print all pages.
[PageWidth](#pagewidth) | The page width in inches.
[PagesPerSide](#pagesperside) | Prints multiple pages of a document on a single piece of paper. Choose from 1, 2, 4, 6, 9 or 16.
[PrinterName](#printername) | The name of the printer to use.
[ScaleFactor](#scalefactor) | The scale factor is a value between 0.1 and 2.0.
[ShouldPrintBackgrounds](#shouldprintbackgrounds) | `true` if background colors and images should be printed.
[ShouldPrintHeaderAndFooter](#shouldprintheaderandfooter) | `true` if header and footer should be printed.
[ShouldPrintSelectionOnly](#shouldprintselectiononly) | `true` if only the current end user's selection of HTML in the document should be printed.

## Properties

### Collation

>  [CoreWebView2PrintCollation](corewebview2printcollation.md) Collation

Printer collation.
See [CoreWebView2PrintCollation](corewebview2printcollation.md) for descriptions of collation. The default value is [CoreWebView2PrintCollation](corewebview2printcollation.md).Default.

Printing uses default value of printer's collation if an invalid value is provided for the specific printer.

This value is ignored in [CoreWebView2.PrintToPdfStreamAsync](corewebview2.md#printtopdfstreamasync) method.

### ColorMode

>  [CoreWebView2PrintColorMode](corewebview2printcolormode.md) ColorMode

Printer color mode.
See [CoreWebView2PrintColorMode](corewebview2printcolormode.md) for descriptions of color modes. The default value is [CoreWebView2PrintColorMode](corewebview2printcolormode.md).Default.

Printing uses default value of printer supported color if an invalid value is provided for the specific printer.

### Copies

>  int Copies

Number of copies to print. Minimum value is `1` and the maximum copies count is `999`.
The default value is 1.

### Duplex

>  [CoreWebView2PrintDuplex](corewebview2printduplex.md) Duplex

Printer duplex settings.
See [CoreWebView2PrintDuplex](corewebview2printduplex.md) for descriptions of duplex. The default value is [CoreWebView2PrintDuplex](corewebview2printduplex.md).Default.

Printing uses default value of printer's duplex if an invalid value is provided for the specific printer.

This value is ignored in [CoreWebView2.PrintToPdfStreamAsync](corewebview2.md#printtopdfstreamasync) method.

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
The default is 1 cm, or ~0.4 inches. A margin cannot be less than zero. If an invalid value is provided, the current value is not changed and an ArgumentException is thrown.

### MarginLeft

>  double MarginLeft

The left margin in inches.
The default is 1 cm, or ~0.4 inches. A margin cannot be less than zero. If an invalid value is provided, the current value is not changed and an ArgumentException is thrown.

### MarginRight

>  double MarginRight

The right margin in inches.
The default is 1 cm, or ~0.4 inches. A margin cannot be less than zero. If an invalid value is provided, the current value is not changed and an ArgumentException is thrown.

### MarginTop

>  double MarginTop

The top margin in inches.
The default is 1 cm, or ~0.4 inches. A margin cannot be less than zero. If an invalid value is provided, the current value is not changed and an ArgumentException is thrown.

### MediaSize

>  [CoreWebView2PrintMediaSize](corewebview2printmediasize.md) MediaSize

Printer media size.
See [CoreWebView2PrintMediaSize](corewebview2printmediasize.md) for descriptions of media size. The default value is [CoreWebView2PrintMediaSize](corewebview2printmediasize.md).Default.

If media size is [CoreWebView2PrintMediaSize](corewebview2printmediasize.md).Custom, you should set the PageWidth and PageHeight.

Printing uses default value of printer supported media size if an invalid value is provided for the specific printer.

This value is ignored in [CoreWebView2.PrintToPdfStreamAsync](corewebview2.md#printtopdfstreamasync) method.

### Orientation

>  [CoreWebView2PrintOrientation](corewebview2printorientation.md) Orientation

The orientation can be portrait or landscape.
The default orientation is portrait. See [CoreWebView2PrintOrientation](corewebview2printorientation.md).

### PageHeight

>  double PageHeight

The page height in inches.
The default height is 11 inches. If the provided page height is less than or equal to zero, the current value is not changed and an ArgumentException is thrown.

### PageRanges

>  string PageRanges

Page range to print. Defaults to empty string, which means print all pages.
The PageRanges property is a list of page ranges specifying one or more pages that should be printed separated by commas. Any whitespace between page ranges is ignored.
A valid page range is either a single integer identifying the page to print, or a range in the form `[start page]-[last page]` where `start page` and `last page` are integers identifying the first and last inclusive pages respectively to print.
Every page identifier is an integer greater than 0 unless wildcards are used (see below examples).
The first page is 1.

In a page range of the form `[start page]-[last page]` the start page number must be larger than 0 and less than or equal to the document's total page count.
If the `start page` is not present, then 1 is used as the `start page`.
The `last page` must be larger than the `start page`.
If the `last page` is not present, then the document total page count is used as the `last page`.

Repeating a page does not print it multiple times. To print multiple times, use the [CoreWebView2PrintSettings.Copies](corewebview2printsettings.md#copies) property.

The pages are always printed in ascending order, even if specified in non-ascending order.

If page range is not valid or if a page is greater than document total page count, ArgumentException is thrown.

The following examples assume a document with 20 total pages.

|       Example         |       Result      |               Notes                                              |
| --- | --- | --- |
| "2"                   |  Page 2           |                                                                  |
| "1-4, 9, 3-6, 10, 11" |  Pages 1-6, 9-11  |                                                                  |
| "1-4, -6"             |  Pages 1-6        | The "-6" is interpreted as "1-6".                                |
| "2-"                  |  Pages 2-20       | The "2-" is interpreted as "pages 2 to the end of the document". |
| "4-2, 11, -6"         |  Invalid          | "4-2" is an invalid range.                                       |
| "-"                   |  Pages 1-20       | The "-" is interpreted as "page 1 to the end of the document".   |
| "1-4dsf, 11"          |  Invalid          |                                                                  |
| "2-2"                 |  Page 2           |                                                                  |

### PageWidth

>  double PageWidth

The page width in inches.
The default width is 8.5 inches. If the provided page width is less than or equal to zero, the current value is not changed and an ArgumentException is thrown.

### PagesPerSide

>  int PagesPerSide

Prints multiple pages of a document on a single piece of paper. Choose from 1, 2, 4, 6, 9 or 16.
The default value is 1.

If an invalid value is provided, ArgumentException is thrown.

Below examples shows print output for PagesPerSide and Duplex.

|  PagesPerSide   |    Total pages   | Two-sided printing  |              Result                                               |
| --- | --- | --- | --- |
|      1          |      1           |        -            | 1 page on the front side.                                         |
|      2          |      1           |        Yes          | 1 page on the front side.                                         |
|      2          |      4           |        -            | 2 pages on the first paper and 2 pages on the next paper.         |
|      2          |      4           |        Yes          | 2 pages on the front side and 2 pages on back side.               |
|      4          |      4           |        Yes          | 4 pages on the front side.                                        |
|      4          |      8           |        Yes          | 4 pages on the front side and 4 pages on the back side.           |

### PrinterName

>  string PrinterName

The name of the printer to use.
Defaults to empty string. If the printer name is empty string or null, then it prints to the default printer on the user OS.

If provided printer name doesn't match with the name of any installed printers on the user OS, the method returns with [CoreWebView2PrintStatus](corewebview2printstatus.md).PrinterUnavailable.

Use [DeviceInformation.FindAllAsync](/uwp/api/windows.devices.enumeration.deviceinformation.findallasync) to get the list of local printers with AQS as "System.Devices.HardwareIds:~~"PRINTENUM\LocalPrintQueue""

This value is ignored in [CoreWebView2.PrintToPdfStreamAsync](corewebview2.md#printtopdfstreamasync) method.

### ScaleFactor

>  double ScaleFactor

The scale factor is a value between 0.1 and 2.0.
The default is 1.0. If an invalid value is provided, the current value is not changed and an ArgumentException is thrown.

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
