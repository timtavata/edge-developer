---
description: Distribution options when releasing an app using Microsoft Edge WebView2
title: Distribution of Microsoft Edge WebView2 Application
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, wpf apps, wpf, edge, ICoreWebView2, ICoreWebView2Host, browser control, edge html
---

# Distribution of Applications using WebView2


**With the 2 version models. Both require effort from a developer for distribution. This article outlines the steps and evaluation a dev must do when distributing an application using WebView2.**

## Browser Channels

Developers can target different [channels](https://www.microsoftedgeinsider.com/download/) of the Microsoft Edge (Chromium) browser to power the WebView2 control. In most cases, production applications should target the Stable channel, but developers often need to test on Beta, Dev, or Canary to ensure their applications continue to work in the near future. The WebView2 API allows developers to programmatically target either the most stable or the least stable channel installed on users’ machine. Alternatively, developers can also use the below registry key to enforce a channel. See more details in [CreateWebView2EnvironmentWithDetails](webview2/reference/webview2.idl.md) function.


## App Distribution
The WebView2 control utilizes the Microsoft Edge (Chromium) browser. When distributing your app it is important to ensure that the Edge browser is installed on all user machines where your application will run. You should also be aware of which version and channel is installed, e.g. Stable, Beta, Dev, or Canary. The WebView2 controller will utilize the most stable version of the browser when installed on a machine.

### Future Planned Changes

We recognize that the Edge browser may not be available on all user machines your application is intended to run, or that control of the Edge browser install process may be difficult. To ensure your application will run on all machines, independent of the install status of the client Microsoft Edge browser, we will release the Microsoft Edge WebView2 Runtime. We will further update WebView2 to search for the stable version of the Runtime before searching for pre-release versions of the installed browser.

We also recognize that some app developers operate in constrained environments, and so intend to support two distribution options, evergreen and fixed version.

Evergreen is the recommended distribution model for most developers. In this mode updates to the WebView2 Runtime will be fully managed by Microsoft keeping you up to date automatically without additional effort from your application. With this self-updating model you can be assured that your app is taking advantage of the latest features and security updates for hosted web content.

For constrained environments we will also support a fixed version distribution model. In this model your application will select and package a specific WebView2 version. Updates to the WebView version will be the responsibility of the application and will be independent of any managed Microsoft update mechanisms. You should choose this model if it is crucial to be able to have absolute control over the browser version and update times your application is taking advantage of.

## Microsoft Edge WebView2 Runtime

The Microsoft Edge WebView2 Runtime is a packaging of the browser binaries optimized for use by WebView2 applications. It will function stand alone or side-by-side with a client Edge Browser install. A single install of the run-time will support any number of WebView2 applications. Install of the runtime will not appear as a browser install to end-user, i.e. no desktop shortcuts, start menu entry, or protocol registration.

An application utilizing WebView2 must ensure the installation of the Microsoft Edge WebView2 Runtime has occurred. At application install time you should check the current install status, which can be determined by using [GetAvailableCoreWebView2BrowserVersionString](webview2/reference/webview2.idl.md#getavailablecorewebview2browserversionstring)s
. If the WebView2 Runtime is not available, you should chain the Microsoft Edge WebView2 Runtime Installer to your install flow.

## Feedback

If something is unclear, please let us know! Visit our [feedback repo](https://aka.ms/webviewfeedback) to ask us a question, submit feature requests, or bug reports. 