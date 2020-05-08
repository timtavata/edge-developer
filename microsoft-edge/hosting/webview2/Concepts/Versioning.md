---
description: Versioning Models used for Microsoft Edge WebView2
title: Versioning of Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, wpf apps, wpf, edge, ICoreWebView2, ICoreWebView2Host, browser control, edge html
---

# Versioning of WebView2

The version of the WebView2 SDK matches the version of the Browser. The Chromium browser updates every 6 weeks. These updates vary from new web platform functionality to security patches and bug fixes. The cadence is controlled by the Chromium project.

## Evergreen vs. Fixed (Bring-Your-Own)
The WebView2 control relies on the Microsoft Edge (Chromium) browser and currently has an evergreen distribution model – instead of packaging a browser in the app bundle, apps use the evergreen browser installed on users’ machines. The evergreen browser updates itself on a regular cadence, therefore apps targeting the evergreen WebView2 automatically get the latest feature and security updates for hosted web content. The WebView2 SDK is updated separately as new APIs become available. This is the recommended model for most developers. 

In the future, there will be a second bring-your-own (BYO) option that allows developers to bundle a redistributable version of the browser with their apps. BYO brings a locked platform, but requires a larger disk footprint for the packaged browser and developers will have to take on the responsibility of servicing and updating the control themselves.

## Browser Channels

Developers can target different [channels](https://www.microsoftedgeinsider.com/download/) of the Microsoft Edge (Chromium) browser to power the WebView2 control. In most cases, production applications should target the Stable channel, but developers often need to test on Beta, Dev, or Canary to ensure their applications continue to work in the near future. The WebView2 API allows developers to programmatically target either the most stable or the least stable channel installed on users’ machine. Alternatively, developers can also use the below registry key to enforce a channel. See more details in [CreateWebView2EnvironmentWithDetails](webview2/reference/webview2.idl.md) function.

## Microsoft Edge WebView2 Runtime

The Microsoft Edge WebView2 Runtime is a packaging of the browser binaries optimized for use by WebView2 applications. It will function stand alone or side-by-side with a client Edge Browser install. A single install of the run-time will support any number of WebView2 applications. Install of the runtime will not appear as a browser install to end-user, i.e. no desktop shortcuts, start menu entry, or protocol registration.

An application utilizing WebView2 must ensure the installation of the Microsoft Edge WebView2 Runtime has occurred. At application install time you should check the current install status, which can be determined by using [GetAvailableCoreWebView2BrowserVersionString](). If the WebView2 Runtime is not available, you should chain the Microsoft Edge WebView2 Runtime Installer to your install flow.


## Feedback

If something is unclear, please let us know! Visit our [feedback repo](https://aka.ms/webviewfeedback) to ask us a question, submit feature requests, or bug reports. 